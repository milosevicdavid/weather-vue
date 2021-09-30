<script setup>
import { ref } from "vue";
import Card from "./components/Card.vue";
import SearchCard from "./components/SearchCard.vue";

const losangeles = ref(null);
const rio_de_janeiro = ref(null);
const beijing = ref(null);
const search = ref(null);
const searchword = ref("");

function refreshData() {
  LosAngeles();
  Rio();
  Beijing();
  searchCity();
}

function searchCity() {
  fetch(
    `http://api.openweathermap.org/data/2.5/forecast?q=${searchword.value}&units=metric&appid=${process.env.VUE_APP_WEATHER_KEY}`
  )
    .then(response => response.json())
    .then(search_json => (search.value = search_json))
    .catch(error => console.log(error));
}

function LosAngeles() {
  fetch(
    `http://api.openweathermap.org/data/2.5/forecast?units=metric&id=5368361&appid=${process.env.VUE_APP_WEATHER_KEY}`
  )
    .then(la => la.json())
    .then(la_json => (losangeles.value = la_json))
    .catch(error => console.log(error));
}

function Rio() {
  fetch(
    `http://api.openweathermap.org/data/2.5/forecast?units=metric&id=3451190&appid=${process.env.VUE_APP_WEATHER_KEY}`
  )
    .then(rio => rio.json())
    .then(rio_json => (rio_de_janeiro.value = rio_json))
    .catch(error => console.log(error));
}

function Beijing() {
  fetch(
    `http://api.openweathermap.org/data/2.5/forecast?units=metric&id=1816670&appid=${process.env.VUE_APP_WEATHER_KEY}`
  )
    .then(be => be.json())
    .then(be_json => (beijing.value = be_json))
    .catch(error => console.log(error));
}

LosAngeles();
Beijing();
Rio();
</script>

<template>
  <div class="cities-container">
    <div class="cities-wrapper">
      <div class="search-wrapper">
        <h1>Weather Forecast</h1>
        <form @submit.prevent="searchCity">
          <input type="text" v-model="searchword" />
          <button @click="searchCity">SearchCity</button>
          <button @click="refreshData">Refresh</button>
        </form>
      </div>
      <div>
        <SearchCard :city="search" />
      </div>
      <div class="cities">
        <div class="single-city">
          <Card :city="losangeles" />
        </div>
        <div class="single-city">
          <Card :city="rio_de_janeiro" />
        </div>
        <div class="single-city">
          <Card :city="beijing" />
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.search-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.cities {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  padding: 30px;
}

@media (max-width: 750px) {
  .cities {
    flex-direction: column;
  }
}
.cities-wrapper {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  width: 960px;
}

.cities-container {
  display: flex;
  justify-content: center;
}

.single-city {
  margin-top: 100px;
}
</style>

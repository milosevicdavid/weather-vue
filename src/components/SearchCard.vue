<script setup>
import { defineProps, toRefs } from "vue";
const props = defineProps({
  city: Object
});
const { city } = toRefs(props);
</script>

<template>
  <div class="search-city-wrapper">
    <h2 class="city-name">{{ city?.city.name }}</h2>
    <div v-if="city" class="search-city">
      <div class="search-day">
        <div class="title">Today</div>
        <div class="hours">
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[0].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[0].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[0].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>

          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[1].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[1].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[1].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[2].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[2].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[2].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[3].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[3].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[3].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[4].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[4].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[4].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[5].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[5].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[5].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
        </div>
      </div>

      <div class="search-day">
        <div class="title">Tomorrow</div>
        <div class="hours">
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[6].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[6].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[6].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[7].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[7].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[7].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[8].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[8].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[8].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[9].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[9].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[0].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[10].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[10].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[0].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[11].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[11].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[0].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[12].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[12].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[0].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[13].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[13].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[0].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
        </div>
      </div>

      <div class="search-day">
        <div class="title">Day After Tomorrow</div>
        <div class="hours">
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[14].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[14].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[0].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[15].dt_txt.slice(10, -6) }}hh:</span
              >
              {{ parseInt(city?.list[15].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[0].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[16].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[16].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[0].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[17].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[17].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[0].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[18].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[18].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[0].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[19].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[19].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[0].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[20].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[20].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[0].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
          <div class="hour">
            <div>
              <span class="hour-string"
                >{{ city?.list[21].dt_txt.slice(10, -6) }}h:</span
              >
              {{ parseInt(city?.list[21].main.temp) }} °C
            </div>
            <div>
              <img
                :src="
                  `http://openweathermap.org/img/wn/${city?.list[0].weather[0].icon}.png`
                "
                alt="weather
      icon"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.search-city-wrapper {
  text-align: center;
}

.search-city {
  display: flex;
  justify-content: center;
  align-items: center;
}

@media (max-width: 750px) {
  .search-city {
    flex-direction: column;
  }
}

.hour {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
}

.search-day {
  margin: 30px;
  padding: 10px;
  border: 1px solid lightgray;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  width: 150px;
  height: 500px;
}

.title {
  margin-bottom: 20px;
  font-weight: 600;
}

.hour-string {
  font-weight: 600;
}
</style>

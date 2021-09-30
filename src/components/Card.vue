<script setup>
import { defineProps, toRefs } from "vue";
const props = defineProps({
  city: Object
});
const { city } = toRefs(props);
</script>

<template>
  <div v-if="city" class="city">
    <h2 class="city-name">{{ city?.city.name }}</h2>
    <div class="day">
      <div class="title">Today</div>
      <div class="hours">
        <div class="hour">
          <div>
            <span class="hour-string">9h:</span>
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
            <span class="hour-string">12h:</span>
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
            <span class="hour-string">15h:</span>
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
            <span class="hour-string">18h:</span>
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
            <span class="hour-string">21h:</span>
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
            <span class="hour-string">00h:</span>
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

    <div class="day">
      <div class="title">Tomorrow</div>
      <div class="hours">
        <div class="hour">
          <div>
            <span class="hour-string">3h:</span>
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
            <span class="hour-string">6h:</span>
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
            <span class="hour-string">9h:</span>
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
            <span class="hour-string">12h:</span>
            {{ parseInt(city?.list[9].main.temp) }} °C
          </div>
          <div>
            <img
              :src="
                `http://openweathermap.org/img/wn/${city?.list[9].weather[0].icon}.png`
              "
              alt="weather
      icon"
            />
          </div>
        </div>
        <div class="hour">
          <div>
            <span class="hour-string">15h:</span>
            {{ parseInt(city?.list[10].main.temp) }} °C
          </div>
          <div>
            <img
              :src="
                `http://openweathermap.org/img/wn/${city?.list[10].weather[0].icon}.png`
              "
              alt="weather
      icon"
            />
          </div>
        </div>
        <div class="hour">
          <div>
            <span class="hour-string">18h:</span>
            {{ parseInt(city?.list[11].main.temp) }} °C
          </div>
          <div>
            <img
              :src="
                `http://openweathermap.org/img/wn/${city?.list[11].weather[0].icon}.png`
              "
              alt="weather
      icon"
            />
          </div>
        </div>
        <div class="hour">
          <div>
            <span class="hour-string">21h:</span>
            {{ parseInt(city?.list[12].main.temp) }} °C
          </div>
          <div>
            <img
              :src="
                `http://openweathermap.org/img/wn/${city?.list[12].weather[0].icon}.png`
              "
              alt="weather
      icon"
            />
          </div>
        </div>
        <div class="hour">
          <div>
            <span class="hour-string">00h:</span>
            {{ parseInt(city?.list[13].main.temp) }} °C
          </div>
          <div>
            <img
              :src="
                `http://openweathermap.org/img/wn/${city?.list[13].weather[0].icon}.png`
              "
              alt="weather
      icon"
            />
          </div>
        </div>
      </div>
    </div>

    <div class="day">
      <div class="title">Day After Tomorrow</div>
      <div class="hours">
        <div class="hour">
          <div>
            <span class="hour-string">3h:</span>
            {{ parseInt(city?.list[14].main.temp) }} °C
          </div>
          <div>
            <img
              :src="
                `http://openweathermap.org/img/wn/${city?.list[14].weather[0].icon}.png`
              "
              alt="weather
      icon"
            />
          </div>
        </div>
        <div class="hour">
          <div>
            <span class="hour-string">6h:</span>
            {{ parseInt(city?.list[15].main.temp) }} °C
          </div>
          <div>
            <img
              :src="
                `http://openweathermap.org/img/wn/${city?.list[15].weather[0].icon}.png`
              "
              alt="weather
      icon"
            />
          </div>
        </div>
        <div class="hour">
          <div>
            <span class="hour-string">9h:</span>
            {{ parseInt(city?.list[16].main.temp) }} °C
          </div>
          <div>
            <img
              :src="
                `http://openweathermap.org/img/wn/${city?.list[16].weather[0].icon}.png`
              "
              alt="weather
      icon"
            />
          </div>
        </div>
        <div class="hour">
          <div>
            <span class="hour-string">12h:</span>
            {{ parseInt(city?.list[17].main.temp) }} °C
          </div>
          <div>
            <img
              :src="
                `http://openweathermap.org/img/wn/${city?.list[17].weather[0].icon}.png`
              "
              alt="weather
      icon"
            />
          </div>
        </div>
        <div class="hour">
          <div>
            <span class="hour-string">15h:</span>
            {{ parseInt(city?.list[18].main.temp) }} °C
          </div>
          <div>
            <img
              :src="
                `http://openweathermap.org/img/wn/${city?.list[18].weather[0].icon}.png`
              "
              alt="weather
      icon"
            />
          </div>
        </div>
        <div class="hour">
          <div>
            <span class="hour-string">18h:</span>
            {{ parseInt(city?.list[19].main.temp) }} °C
          </div>
          <div>
            <img
              :src="
                `http://openweathermap.org/img/wn/${city?.list[19].weather[0].icon}.png`
              "
              alt="weather
      icon"
            />
          </div>
        </div>
        <div class="hour">
          <div>
            <span class="hour-string">21h:</span>
            {{ parseInt(city?.list[20].main.temp) }} °C
          </div>
          <div>
            <img
              :src="
                `http://openweathermap.org/img/wn/${city?.list[20].weather[0].icon}.png`
              "
              alt="weather
      icon"
            />
          </div>
        </div>
        <div class="hour">
          <div>
            <span class="hour-string">00h:</span>
            {{ parseInt(city?.list[21].main.temp) }} °C
          </div>
          <div>
            <img
              :src="
                `http://openweathermap.org/img/wn/${city?.list[21].weather[0].icon}.png`
              "
              alt="weather
      icon"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.city {
  display: flex;
  flex-direction: column;
}

.hour {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.day {
  margin-top: 35px;
  padding: 10px;
  border: 1px solid lightgray;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.title {
  margin-bottom: 20px;
  font-weight: 600;
}

.hour-string {
  font-weight: 600;
}
</style>

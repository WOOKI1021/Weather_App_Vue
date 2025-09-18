<script setup>
const convertCelcius = (kelvin) => {
  return (kelvin - 273.15).toFixed(1);
};
</script>

<template>
  <div class="weather-info">
    <div class="icon">
      <img
        :src="`https://openweathermap.org/img/wn/${$store.state.weatherData.icon}@2x.png`"
        :alt="$store.state.weatherData.icon"
      />
    </div>
    <div class="temp">
      {{ convertCelcius($store.state.weatherData.temp) }}°C
    </div>
    <div class="text">
      {{ $store.state.weatherData.text }}
    </div>
    <div class="location">
      <font-awesome-icon :icon="['fas', 'location-dot']" />
      <span>&nbsp;&nbsp;&nbsp;{{ $store.state.weatherData.city }}&nbsp;,&nbsp;&nbsp;{{ $store.state.weatherData.location }}</span
      >
    </div>
  </div>
</template>

<style scoped lang="scss">
.weather-info {
  padding: 10px;
  & > div {
    margin-bottom: 10px;
    padding: 20px;
    
  }
  .icon img {
    width: 140px;
  }
  .temp {
    font-size: 4em;
  }
  .text {
    font-size: 2em;
  }
  .tab-indent {
    padding-left: 2em; /* 또는 margin-left: 2em; */
  }
}
</style>

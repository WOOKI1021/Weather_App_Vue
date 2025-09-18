<script setup>
import SearchBar from './SearchBar.vue';
import Weatherinfo from './Weatherinfo.vue';

</script>

<template>
  <div class="container">
    <SearchBar />
    <Weatherinfo />
  </div>
</template>

<style scoped>
  .container {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
}
</style>
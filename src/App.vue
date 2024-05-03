<script setup>
import TheHeader from './components/TheHeader.vue'
import TheSearch from './components/TheSearch.vue'
import TheInformation from './components/TheInformation.vue'
import { ref } from 'vue'

const items = ref([])

const getItems = async () => {
  const response = await fetch('https://jsonplaceholder.typicode.com/users')
  const data = await response.json()
  items.value = data
}
</script>

<template>
  <div class="app">
    <TheHeader />
    <div class="main">
      <TheSearch />
      <TheInformation />
    </div>
  </div>
</template>

<style lang="scss">
@import './assets/main.scss';
</style>

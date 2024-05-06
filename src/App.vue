<script setup>
import TheHeader from './components/TheHeader.vue'
import TheSearch from './components/TheSearch.vue'
import TheInformation from './components/TheInformation.vue'
import axios from 'axios'
import { onMounted, reactive, ref } from 'vue'

// const items = ref([])
// const filters = reactive({
//   sortBy: 'name',
//   search: ''
// })

// const onChangeSearchInput = (e) => {
//   filters.search = e.target.value
// }
// const fetchItems = async () => {
//   try {
//     const params = {
//       sortBy: filters.sortBy
//     }
//     if (filters.search) {
//       params.title = `*${filters.search}*`
//     }
//     const { data } = await axios.get('https://jsonplaceholder.typicode.com/users', { params })
//     items.value = data
//   } catch (error) {
//     console.log(error)
//   }
// }
// onMounted(() => {
//   fetchItems()
// })
</script>

<template>
  <div class="app">
    <TheHeader />
    <div class="main">
      <TheSearch :onChangeSearchInput="onChangeSearchInput" />
      <TheInformation />
    </div>
  </div>
</template>

<style lang="scss">
@import './assets/main.scss';
</style>

<script setup>
import EmployeeCard from './EmployeeCard.vue'
import axios from 'axios'
import { ref } from 'vue'

const nameEmployee = ref('')
const getRequest = async () => {
  const data = await axios.get('https://jsonplaceholder.typicode.com/users', {
    nameEmployee
  })
  const dataEmployee = data.data
  for (let i = 0; i < dataEmployee.length; i++) {
    if (dataEmployee[i].name === nameEmployee.value) {
      console.log(dataEmployee[i])
    }
  }
}
</script>

<template>
  <div class="search">
    <div class="find">
      <h3>Поиск сотрудников</h3>
      <input
        v-model="nameEmployee"
        class="find__input"
        type="text"
        placeholder="Введите id или имя"
      />
      <button class="find__button" @click="getRequest">Найти</button>
    </div>
    <div class="result">
      <h3>Результаты</h3>
      <div class="employee">
        <!-- <p>Начните поиск</p> -->
        <EmployeeCard />
      </div>
    </div>
  </div>
</template>

<style lang="scss">
@import '../assets/SearchStyles.scss';
</style>

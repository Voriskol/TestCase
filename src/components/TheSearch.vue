<script setup>
import EmployeeCard from './EmployeeCard.vue'
</script>

<template>
  <div class="search">
    <div class="find">
      <h3>Поиск сотрудников</h3>
      <input class="find__input" type="text" placeholder="Введите id или имя" />
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

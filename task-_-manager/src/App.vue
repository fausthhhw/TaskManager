<template>
<div>
<h1>Каталог задач</h1>
<div class="tasks">
<TaskCard
v-for="task in tasks"
:Task="task" />

</div>
</div>
</template>
<script setup lang="ts">
import TaskCard from "./components/TaskCard.vue";
const tasks = [
  {id: "1", title: "Погладить кошку", text: "Требуется тщательно погладить кошку. Для выполнения задачи нужна рука (опционально)."},
  {id: "2", title: "Сварить пельмени", text: "Нужно положить в кипящую воду с приправой пятьдесят шесть пельменей."},
  {id: "3", title: "Сыграть в Counter-Strike 2", text: "Включить компьютер, запустить Steam и игру."},
  {id: "4", title: "Купить лимонную воду", text: "Взять со стола сто рублей, сходить в магазин."},
  {id: "5", title: "Выполнить домашние задания", text: "Просмотреть беседу учебной группы, взвесить все за и против, лечь спать."},
]
</script>
<style>
.tasks {
display: flex;
gap: 16px;
flex-direction: column;
}
</style>

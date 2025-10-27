<template>
<div class="Task-Card">
<main>
<div>{{ props.Task.title }}</div>
<div>{{ props.Task.text }}</div>
</main>
<footer>
<button type="button" @click="CompleteTask">Выполнить задачу</button>
</footer>
</div>
</template>
<script setup lang="ts">
const props = defineProps<{
Task: { title: string; text: string};
}>();
function CompleteTask() {
alert(`Поздравляем, вы выполнили задание: ${props.Task.title}`);
}
</script>
<style>
.Task-Card {
display: flex;
gap: 4px;
flex-direction: column;
border: 1px solid #ccc;
padding: 12px;
border-radius: 8px;
}
</style>

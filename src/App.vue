<template>
  <h1>{{ message }}</h1>
  <FoodItem v-model:name="ananas" message="I like"></FoodItem>
</template>

<script setup>
import { ref } from 'vue'
import FoodItem from './components/FoodItem.vue'

const message = ref('This is some text.')
const ananas = ref('Ananas')
</script>

<style scoped></style>

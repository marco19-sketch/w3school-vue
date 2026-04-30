<template>
  <div>
    <div id="container">
      <div id="box">
        <h2>{{ name }}</h2>
        <p>{{ message }} {{ name }}</p>
        <input
          type="text"
          name="fruit"
          id="fruit"
          @input="$emit('update:name', $event.target.value)"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue'

defineProps({
  name: String,
  message: String,
})

defineEmits(['update:name'])

// onMounted(() => {
//   console.log('The FoodItem component is mounted.')
// })
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
#container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
#box {
  background-color: aqua;
  border-radius: 10px;
  padding: 20px;
  width: fit-content;
  display: block;
}
</style>

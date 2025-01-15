<template>
  <div>
    <NewChild @submitName:name="updateTheName" />
    <h1>{{ name }}</h1>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import NewChild from '../components/NewChild.vue'
const name = ref('')
const updateTheName = function (newName) {
  name.value = newName
}
</script>

<style scoped></style>

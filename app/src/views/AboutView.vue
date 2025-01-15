<template>
  <div>
    <NewChild @submitName:name="name" />
    <h1>{{ name }}</h1>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import NewChild from '../components/NewChild.vue'
const name = ref('')
</script>

<style scoped></style>

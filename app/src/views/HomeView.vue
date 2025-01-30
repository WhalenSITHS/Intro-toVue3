<template>
  <LogIn title="Hello Vue" :count="5" :isActive="true"><h1>Using Slots!</h1></LogIn>
  <div class="container">
    <AnimalCard v-for="animal in animals" :key="animal.name" :animal />
  </div>
</template>

<script setup>
import LogIn from '../components/LogIn.vue'
import AnimalCard from '../components/AnimalCard.vue'
const animals = [
  { name: 'Walrus', image: '/walrus.webp' },
  { name: 'Capybara', image: '/capy.jpg' },
]
</script>

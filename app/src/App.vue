<template>
  <div>
    <h1>{{ count }}</h1>
    <button @click="increment">Click Me</button>
    <form name="login-form" @submit.prevent="login(user)">
      <div>
        <label for="username">Username: </label>
        <input id="username" type="text" v-model="user.username" />
      </div>
      <div>
        <label for="password">Password: </label>
        <input id="password" type="password" v-model="user.password" />
      </div>
      <button class="submit-button" type="submit">Login</button>
    </form>
    <div class="animals">
      <h3 v-for="(animal, index) in animals" :key="index">{{ animal }}</h3>
    </div>
    <input v-model="animal" type="text" />
    <button @click="addAnimal(animal)">Add Animal</button>
  </div>
</template>

<script setup>
import { ref, reactive } from 'vue'
function increment() {
  count.value++
}

const count = ref(0)
const user = reactive({ username: '', password: '' })
function login(user) {
  console.log(user)
}
const animals = ref(['Pig', 'Zebra', 'Ox'])
let animal = ''
function addAnimal(animal) {
  animals.value.push(animal)
}
</script>

<style scoped></style>

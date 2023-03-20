<!-- ComponentB.vue -->
<script setup>
import { store } from "../store.js";
</script>

<template>
  <button @click="store.count++">From A: {{ store.count }}</button>
</template>

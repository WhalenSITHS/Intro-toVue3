<!-- ComponentA.vue -->
<script setup>
import { store } from "../store.js";
</script>

<template>
  <button @click="store.count++">From B: {{ store.count }}</button>
</template>

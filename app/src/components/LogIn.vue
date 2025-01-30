<template>
  <div>
    <slot></slot>
    <h1>{{ title }}</h1>
    <p>Count: {{ count }}</p>
    <p v-if="isActive">This is active!</p>
  </div>
</template>

<script setup>
defineProps({
  title: String,
  count: Number,
  isActive: Boolean,
})
</script>

<style scoped></style>

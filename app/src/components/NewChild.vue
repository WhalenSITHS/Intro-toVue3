<template>
  <div>
    <input v-model="name" type="text" />
    <button @click="updateName">Click To Submit</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const name = ref('')
const emit = defineEmits(['submitName'])
const updateName = function () {
  emit('submitName', name.value)
}
</script>

<style lang="scss" scoped></style>

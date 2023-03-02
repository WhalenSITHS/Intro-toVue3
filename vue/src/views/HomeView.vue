<template>
  <h1 v-if="graduated">{{ student }}</h1>
  <h1 v-else>"They have not yet graduated"</h1>
  <h1>{{ student }}</h1>
  <ul>
    <li v-for="animal in animals" :key="animal">{{ animal }}</li>
  </ul>
</template>
<script>
export default {
  data() {
    return {
      student: "Jason",
      animals: ["pig", "cow", "ostrich", "Zee"],
      graduated: true,
    };
  },
};
</script>

<script lang="ts" setup>
const query = ref('');

const search = () => {
  $fetch(`http://www.omdbapi.com/?apikey=a755b202&s=${query.value}`);
};
</script>

<template>
  <form @submit.prevent="search">
    <input type="text" v-model="query" />
    <button>Search</button>
  </form>
</template>

<style scoped></style>

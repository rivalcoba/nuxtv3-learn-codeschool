<script lang="ts" setup>
const query = ref("");

const search = () => {
  $fetch(`http://www.omdbapi.com/?apikey=a755b202&s=${query.value}`);
};
</script>
<template>
  <div class="">
    <div>Page: Movies 🎥</div>
    <form @submit.prevent="search">
      <input type="text" v-model="query" />
      <button>Search</button>
    </form>
  </div>
</template>

<style scoped></style>

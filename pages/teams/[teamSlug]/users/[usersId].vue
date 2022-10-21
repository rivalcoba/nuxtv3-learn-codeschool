<script setup>
const route = useRoute();
// Access paramas on setup
const message = computed(
  () =>
    `I'm on team ${route.params.teamSlug} and my user id is ${route.params.usersId}`
);
</script>

<template>
  <div>
    <p>
      {{ message }}
    </p>
  </div>
</template>

<style scoped></style>

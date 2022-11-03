<template>
  <h1>User:{{ route.params.id }} page</h1>
</template>

<script setup lang="ts">
import { watch } from 'vue';
import { useRoute } from 'vue-router';

const route = useRoute('/users/[id]');

watch(
  () => route.params.id,
  (newId) => console.log(newId),
);
</script>

<style scoped></style>

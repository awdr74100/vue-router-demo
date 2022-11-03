<template>
  <ul>
    <li v-for="(path, index) in paths" :key="index">
      <button @click.prevent="$router.push(path)">{{ path }}</button>
    </li>
  </ul>
</template>

<script setup lang="ts">
const paths = ['/', '/users', '/users/a', '/users/b', '/users/c'];
</script>

<style scoped>
button {
  cursor: pointer;
}
</style>

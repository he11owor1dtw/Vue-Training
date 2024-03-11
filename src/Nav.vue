<script setup>
defineProps(['title','subtitle']);
</script>

<template>
  <div>{{ title }}</div>
  <div>{{ subtitle }}</div>
</template>

<style scoped>
nav {
  padding: 10px;
  background-color: chartreuse;
}
</style>
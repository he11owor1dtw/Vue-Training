<script setup>
defineProps(["backgroundColor", "color"]);
</script>

<template>
  <main :style="{
    color: color,
    backgroundColor: backgroundColor
  }">
    <div @click="change">123</div>
  </main>
</template>

<style scoped></style>
<script setup>
import NavComp from "./Nav.vue";
import MainComp from "./Main.vue";
import { ref } from "vue";
let subtitle = ref("這是網站的副標題");
let updateSubtitle = function () {
  subtitle.value = "這是新的的副標題"
}
</script>

<template>
  <NavComp 
  title="這是網站標題" 
  :subtitle="subtitle">
</NavComp>
  <MainComp 
  backgroundColor="black" 
  color="white" 
  @update="updateSubtitle"
  ></MainComp>
</template>

<style scoped></style>
<script setup>
import MainComp from "./Main.vue";
import { ref } from "vue";
let visible = ref(true);
let hide = function () {
  visible.value = false;
}
let show = function () {
  visible.value = true;
}
</script>

<template>
  <MainComp v-if="visible"></MainComp>
  <button @click="hide">隱藏</button>
  <button @click="show">顯示</button>
</template>

<style scoped></style>
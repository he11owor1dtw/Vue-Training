<script setup>
import { onMounted, onUnmounted, ref } from "vue";
let text = ref("主要的網站內容");
let changeText = function () {
  text.value = "新的網站內容";
};

// 製作一個 Counter 計數器
let counter = ref(0);
let scheduleId;

// 組件掛載時，設定每秒鐘加一的排程
onMounted(function () {
  scheduleId = window.setInterval(function () {
    console.log("每隔一秒鐘,數字加1");
    counter.value = counter.value + 1;
  }, 1000);
});

// 組件卸載時，清除掛載時設定的排程
onUnmounted(function () {
  window.clearInterval(scheduleId);
});
</script>

<template>
  <main>
    <div>{{ counter }}</div>
    <div>{{ text }}</div>
    <button @click="changeText">改變文字</button>
  </main>
</template>

<style scoped></style>

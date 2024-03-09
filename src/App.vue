<script setup>
import { ref } from "vue";
let state = ref({
  title: "網站標題",
  className: "title"
});

let handler = function () {
  state.value.title = "新的網站標題";
  state.value.className = "title highlight";
};
</script>

<template>
  <nav>導覽列</nav>
  <main>
    <div :class="state.className">{{ state.title }}</div>
    <button @click="handler">按鈕</button>
  </main>
</template>

<style scoped>
.title {
  font-weight: bold;
}

.highlight{
  color: blue;
}

main {
  background-color: rgb(113, 223, 155);
}
</style>
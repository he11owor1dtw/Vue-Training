<script setup>
let handler = function () {
  console.log("Click");
}

let mouseoverHandler = function () {
  console.log("Mouse Over");
}
</script>

<template>
  <nav>導覽列</nav>
  <main>
    <button v-on:click="handler">按鈕</button>
    <button @click.once="handler" @mouseover="mouseoverHandler">按鈕</button> <!-- 簡寫 -->
    <a @click.prevent="handler" href="https://he11owor1dtw.github.io/">
      個人網站
    </a> <!-- .prevent 停止超連結並在 console 印出 click -->
  </main>
</template>

<style scoped>
main {
  background-color: rgb(113, 223, 155);
}
</style>
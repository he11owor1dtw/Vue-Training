<script setup>
let level = 0;
let topic = ["HTML", "CSS", "JavaScript", "Vue.js"];  // 陣列
let topics = { html: "HTML", css: "CSS", js: "JavaScript", vue: "Vue.js" };  // 物件
</script>

<template>
  <nav>導覽列</nav>
  <main>
    <div v-if="level === 3">大神</div>
    <div v-else-if="level === 2">資深</div>
    <div v-else-if="level === 1">中階</div>
    <div v-else>
      <div>入門</div>
      <ul>
        <li v-for="(name, index) in topic">
          {{ index }}-{{ name }}
        </li>
      </ul>
    </div>
    <div v-else>
      <div>入門</div>
      <ul>
        <li v-for="(value, key) in topics">  <!-- value=值 , key=鍵 -->
          {{ key }}-{{ value }}
        </li>
      </ul>
    </div>
  </main>
</template>

<style scoped>
main {
  background-color: rgb(113, 223, 155);
}
</style>
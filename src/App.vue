<script setup>
let message = "<u>Hello Vue</u>";
let name = "content";
let checked = false;
</script>

<template>
  <nav>導覽列</nav>
  <main v-html="message.toUpperCase()"></main> <!--增加程式語句 -->
  <main>{{ message.toUpperCase() }}</main> <!--增加程式語句 -->
  <div :class="name">操作標籤的屬性</div>
  <div :class="checked?'dark':'light'">操作標籤的屬性</div> <!--增加程式語句 JS三元運算式 -->
</template>

<style scoped>
main {
  background-color: rgb(190, 190, 190);
}

.content {
  color: blue;
}

.dark{
  color: rgb(190, 22, 22);
}

.light{
  color: rgb(66, 197, 197);
}
</style>
<script setup>
defineProps(["backgroundColor", "color"]);
// 方法2 利用js
let emit = defineEmits(["update"]);
let updateParentSubtitle = function () {
  emit("update")
}
</script>

<template>
  <main :style="{
    color: color,
    backgroundColor: backgroundColor
  }">
    <div @click="change">123</div>
    <!-- <button @click="$emit('update')">改變副標題</button> 方法1 -->
    <button @click="updateParentSubtitle">改變副標題</button>
  </main>
</template>

<style scoped></style>
<script setup>
// 資料串接網址 https://cwpeng.github.io/live-records-samples/data/products.json
import { onMounted, ref } from "vue";
import List from "./List.vue";
// 建立響應式狀態 products 一開始是空值 null
let products = ref(null);

// 組件掛載完成後，開始呼叫 fetch 串接後端的資料
onMounted(async function () {
  let response = await fetch("https://cwpeng.github.io/live-records-samples/data/products.json")
  let data = await response.json();
  // console.log(data);
  products.value = data;
})
</script>

<template>
  <div class="headline">產品資料列表</div>
  <div v-if="products === null">資料載入中</div>
  <List v-else :products="products"></List>
</template>

<style scoped>
.headline {
  font-size: 20px;
  font-weight: bolder;
}


</style>
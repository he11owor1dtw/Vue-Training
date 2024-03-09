<script setup>
import { ref } from "vue";
let content = ref('');
let clearContent = function () {
  content.value = "";
}
let interests = ref([]);
let color = ref(null);
let option = ref("");
</script>

<template>
  <nav>導覽列</nav>
  <main>
    <h3>單行輸入框</h3>
    <input type="text" v-model="content">
    <div>使用者輸入的文字是：{{ content }}</div>
    <button @click="clearContent">清空輸入框</button>
    <hr>

    <h3>多選框</h3>
    角色扮演 <input type="checkbox" value="rpg" v-model="interests">
    即時戰略 <input type="checkbox" value="rts" v-model="interests">
    動作遊戲 <input type="checkbox" value="action" v-model="interests">
    <!-- <div>喜歡的遊戲類型是：{{ interests }}</div>  將陣列顯示給使用者看 UX差 -->
    <ul>
      <li v-for="interest in interests">{{ interest }}</li>
    </ul>
    <hr>

    <h3>單選框</h3>
    紅色 <input type="radio" value="red" v-model="color">
    綠色 <input type="radio" value="green" v-model="color">
    藍色 <input type="radio" value="blue" v-model="color">
    <div :class="color">這是一段文字：{{ color }}</div> <!-- 與 class 屬性連動 -->
    <hr>
    
    <h3>下拉式選單</h3>
    <select v-model="option">
      <option value="">請選擇顏色</option>
      <option value="yellow">黃色</option>
      <option value="black">黑色</option>
      <option value="white">白色</option>
    </select>
    <div :class="option">使用者選擇的顏色是：{{ option }}</div>
  </main>
</template>

<style scoped>
main {
  background-color: rgb(113, 223, 155);
}

.red {
  color: red;
}

.green {
  color: green;
}

.blue {
  color: blue;
}

.yellow {
  color: yellow;
}

.black {
  color: black;
}

.white {
  color: white;
}
</style>
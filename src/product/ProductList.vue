<script setup>
defineProps(['products']);
</script>

<template>
  <div class="list">
    <div class="product" v-for="product in products">
      <div class="name">{{ product.name }}</div>
      <div class="price">價格：{{ product.price }}</div>
      <div class="description">{{ product.description }}</div>
    </div>
  </div>
</template>

<style scoped>
.list {
  line-height: 1.5rem;
}

.product {
  padding: 15px 0px;
  border-bottom: 1px solid lightgray;
}

.name {
  font-weight: bolder;
}
</style>
<script setup lang="ts">
import type { Product } from '@/models/products'

defineProps<{
  product: Product
}>()
</script>

<template>
  <div class="box">
    <div class="box-large">
      <img :src="product.thumbnail" alt="product.name" />
    </div>
    <div class="box-content">
      <h3>{{ product.title }}</h3>
      <i>{{ product.brand }}</i>
      <p>{{ product.description }}</p>
      <p class="price">${{ product.price }}</p>
      <button class="button is-success">Add to Cart</button>
    </div>
  </div>
</template>

<style scoped>
h3 {
  font-weight: bold;
}
i {
  color: whitesmoke;
}
.price {
  color: azure;
  font-size: 1.5rem;
  float: right;
  font-weight: bold;
}
.shelf .box {
  width: 17rem;
  flex-grow: 1;
}
</style>

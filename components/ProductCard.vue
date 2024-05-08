<template>
  <div class="card text-center">
    <img :src="product.image" alt="product thump" class="thumb">
    <p class="font-bold text-gray-500 m4 truncante title">{{ product.title }}</p>
    <nuxt-link :to="`./products/${product.id}`">
      <p class="btn my-4">View Details</p>
    </nuxt-link>
  </div>
</template>

<script setup>

  const {product} = defineProps(['product'])
</script>

<style  scoped>
  .thumb{
    max-width: 70%;
    height: 120px;
    object-fit: cover;
    margin: 20px auto;
  }
  .title{
    margin:10px 10px;
  }
</style>
<template>
  <div class="card">
    <div class="flex gap-10 h-52">
      <div class="p-7 flex content-center items-center">
        <img :src="product.image" alt="product img"  class="mx-auto my-7 h-full ">
      </div>
      <div class="p-7  ">
        <h2 class="text-4x1 my-7">{{ product.title }}</h2>
        <p class="text-x1 my-7"> category - {{ product.category }}</p>
        <p class="text-x1 my-7"> price - ${{ product.price }}</p>
        <h3 class="font-bold border-b-2 mb-4 pb-2"> Product Description</h3>
        <p class="mb-7">{{ product.description }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
const { product } = defineProps(["product"]);

</script>

<style  scoped>
.line{
  border:red 1px solid;
}
</style>
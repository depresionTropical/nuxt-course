<template>
  <div >
    <ProductDetail :product="product" />
  </div>

</template>

<script setup>
const { id } = useRoute().params;
const uri = `https://fakestoreapi.com/products/${id}`;
definePageMeta({
  layout: "products",
});
</script>

<style  scoped>

</style>
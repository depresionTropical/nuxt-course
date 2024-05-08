<template>
  <div >
    <ProductDetail :product="product" />
  </div>
  <div class="grid grid-cols-4  gap-5">
    <div v-for="p in categoryProducts" :key="p.id">
      <ProductCard :product="p" />
    </div>
  </div>
</template>

<script setup>
const { id } = useRoute().params;
const uri = `https://fakestoreapi.com/products/${id}`;
const { data: product } = await useFetch(uri);
console.log(product[category]);
const { data: categoryProducts } = await useFetch(`https://fakestoreapi.com/products/category/${product[category]}`);

definePageMeta({
  layout: "products",
});
</script>

<style  scoped>

</style>
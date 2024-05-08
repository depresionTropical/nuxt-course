<template>
 <div>
  <h2>Products</h2>
  <div class="grid grid-cols-4  gap-5">
    <div v-for="p in products" :key="p.id">
      <ProductCard :product="p" />
    </div>
  </div>
 </div>
</template>

<script setup>

  definePageMeta({
    layout : 'products'
  });
  // fetch data from the API
  const {data: products} =await useFetch('https://fakestoreapi.com/products')
</script>
<style  scoped>
h2{
  margin: 20px;
  font-size: 36px;

}

p{
  margin: 20px;
  font-size: 18px;
  line-height: 1.5;
}

</style>
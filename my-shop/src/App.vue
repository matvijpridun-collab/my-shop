<template>
  <div id="app">
    <ProductCard
      img="https://img.magnific.com/premium-photo/blank-black-tshirt-mockup-clothing-design_1032986-274895.jpg?semt=ais_hybrid&w=740&q=80"
      name="футболка чорна"
      description="бавовняна футболка чорного кольору, розмір M"
      :price="450"
    />
  </div>
</template>

<script>
import ProductCard from './product.card.vue'

export default {
  components: {
    ProductCard
  }
}
</script>

<style>
#app {
  padding: 16px;
}
</style>
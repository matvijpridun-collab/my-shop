<template>
<div class="product-card">
  <img class="product-image" :src="img" :alt="product.name" />
  <h2 class="product-name">{{ product.name }}</h2>
  <p class="product-description">{{ product.description }}</p>
  <p class="product-price">{{ product.price | currency }}</p>
  <button class="buy-button">купити</button>
</div>
</template>


<script>
export default {
   name: 'ProductCardComponent',
   props: {
   name: String,
   description: String,
   price: Number,
   img: String
  }
}
 

</script>

<style></style>
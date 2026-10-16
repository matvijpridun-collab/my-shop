<template>
<div class="product-card">
  <img v-if="img" class="product-image" :src="img" :alt="name" />
  <h2 class="product-name">{{ name }}</h2>
  <p class="product-description">{{ description }}</p>
  <p class="product-price">{{ price }} грн</p>
     <button class="buy-button">купити</button>
</div>
</template>


<script>
export default {
   name: 'ProductCardComponent',
   props: {
   name: {
     type: String,
     required: true
   },
   description: {
     type: String,
     required: true
   },
   price: {
     type: Number,
     required: true
   },
   img: {
     type: String,
     default: ''
   }
  }
}
 

</script>

<style>
html {
  margin: 0;
  padding: 0;
  background-color: #482020;
}

body {
  min-height: 100vh;
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
  color: #f0efef;
  background: linear-gradient(135deg, #5f3737, #482020);
}
* {
  box-sizing: border-box;
}
.product-card {
  background-color: #302a2a;
  border: none;
  border-radius: 12px;
  padding: 16px;
  text-align: center;
  width: 300px;
  margin: 16px auto;
}
.product-image {
  width: 100%;
  height: auto;
  border-radius: 16px;
}
.product-name {
  font-size: 1.5em;
  margin: 8px 0;
}
.product-description {
  font-size: 1em;
  color: #ededed;
  margin: 8px 0;
}
.product-price {
  font-size: 1.2em;
  color: #e5e5e5;
  margin: 8px 0;
}
.buy-button {
  position: relative;
  overflow: hidden;
  background: linear-gradient(135deg, #32c85a, #218838);
  color: white;
  border: none;
  padding: 11px 24px;
  font-size: 1em;
  font-weight: 700;
  cursor: pointer;
  border-radius: 8px;
  box-shadow: 0 4px 10px rgba(33, 136, 56, 0.28);
  transition: transform 0.2s ease, box-shadow 0.2s ease, filter 0.2s ease;
}
.buy-button::after {
  content: "";
  position: absolute;
  top: -50%;
  left: -60%;
  width: 35%;
  height: 200%;
  background: rgba(255, 255, 255, 0.25);
  transform: rotate(25deg);
  transition: left 0.45s ease;
}
.buy-button:hover {
  filter: brightness(1.08);
  transform: translateY(-3px) scale(1.03);
  box-shadow: 0 8px 18px rgba(33, 136, 56, 0.38);
}
.buy-button:hover::after {
  left: 130%;
}
.buy-button:active {
  filter: brightness(0.94);
  transform: translateY(0) scale(0.98);
  box-shadow: 0 2px 6px rgba(33, 136, 56, 0.28);
}
.buy-button:focus-visible {
  outline: 3px solid #a7f3b6;
  outline-offset: 3px;
}
@media (prefers-reduced-motion: reduce) {
  .buy-button,
  .buy-button::after {
    transition: none;
  }
}

</style>
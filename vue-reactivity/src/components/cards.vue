<template>
  <div class="product">
    <img :src="img" :alt="name" />
    <h3>{{ name }}</h3>
    <h4>{{ group }}</h4>
    <h5>{{ price }}</h5>
    <button @click="addToCart(name, group, price, img)" class="cart-button">
      Add to Cart
    </button>
  </div>
</template>

<script setup>
import { defineProps } from "vue";
import { store } from "../store.js";
const props = defineProps({
  name: String,
  group: String,
  price: String,
  img: String,
});

function addToCart(name, group, price, img) {
  const item = {
    name: name,
    group: group,
    price: price,
    img: img,
  };
  store.cart.push(item);
}
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Dongle:wght@300;400;700&display=swap");

* {
  font-family: "Dongle", sans-serif;
}
.product {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 30%;
}

img {
  width: 80%;
}
h3 {
  font-size: 30px;
}
h4 {
  font-size: 25px;
}
h5 {
  font-size: 20px;
}
.cart-button {
  font-size: 20px;
}
</style>

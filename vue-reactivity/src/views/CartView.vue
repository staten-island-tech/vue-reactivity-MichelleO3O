<template>
  <h1>Your Cart</h1>
  <h2>Total Cost: {{ calculateprice(cart) }}</h2>
  <h3>Number of Items in Cart: {{ number }}</h3>
  <div class="items">
    <div class="albumsInCart" v-for="(item, index) in cart">
      <img :src="item.img" :alt="item.name" />
      <h4>{{ item.name }}</h4>
      <h5>{{ item.group }}</h5>
      <h6>{{ item.price }}</h6>
      <button @click="removeitemfromcart(item.name)">Remove Item</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { store } from "../store.js";
const cart = ref(store.cart);
const number = ref(cart.value.length);

function calculateprice(cart) {
  let price = 0;
  for (let item of cart) {
    price += parseFloat(item.price.slice(1));
  }
  price = Math.ceil(price).toFixed(2);
  return price;
}

function removeitemfromcart(name) {
  cart.value.splice(
    cart.value.findIndex((item) => item.name === name),
    1
  );
  number.value -= 1;
}
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Dongle:wght@300;400;700&display=swap");
* {
  font-family: "Dongle", sans-serif;
}
.items {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.albumsInCart {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 30%;
}

img {
  width: 80%;
}

h4 {
  font-size: 30px;
}
h5 {
  font-size: 25px;
}
h6 {
  font-size: 20px;
}
</style>

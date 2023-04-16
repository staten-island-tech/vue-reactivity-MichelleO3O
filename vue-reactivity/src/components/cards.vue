<template>
  <div class="product">
    <img :src="img" :alt="name" />
    <h3>{{ name }}</h3>
    <h4>{{ group }}</h4>
    <h5>{{ price }}</h5>
  </div>
</template>

<script>
import { defineProps } from "vue";
export default {
  props: {
    name: String,
    group: String,
    price: String,
    img: String,
  },
};
</script>

<style scoped>
.product {
  width: 60%;
  margin-left: 10%;
}

img {
  width: 80%;
}
</style>

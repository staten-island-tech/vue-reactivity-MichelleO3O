<template>
  <div class="product">
    <img :src="props.img" :alt="props.name" />
    <h3>{{ props.name }}</h3>
    <h4>{{ props.group }}</h4>
    <h5>{{ props.price }}</h5>
  </div>
</template>

<script setup>
import { defineProps } from "vue";
defineProps({
  name: String,
  group: String,
  price: String,
  img: String,
});
</script>

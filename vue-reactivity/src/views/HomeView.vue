<template>
  <div class="title"><h1>Album Shop</h1></div>
  <cards
    v-for="(album, index) in albums"
    :name="album.name"
    :group="album.group"
    :price="album.price"
    :img="album.img"
  >
  </cards>
</template>

<script setup>
import cards from "../components/cards.vue";

const albums = [
  { name: "Ready To Be", group: "Twice", price: "$25.99", img: "" },
  { name: "", group: "", price: "", img: "" },
  { name: "", group: "", price: "", img: "" },
  { name: "", group: "", price: "", img: "" },
  { name: "", group: "", price: "", img: "" },
  { name: "", group: "", price: "", img: "" },
  { name: "", group: "", price: "", img: "" },
  { name: "", group: "", price: "", img: "" },
  { name: "", group: "", price: "", img: "" },
  { name: "", group: "", price: "", img: "" },
  { name: "", group: "", price: "", img: "" },
];
</script>

<style lang="scss" scoped></style>

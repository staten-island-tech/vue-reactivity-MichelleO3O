<template>
  <div class="title"><h1>Album Shop</h1></div>
  <cards
    v-for="(album, index) in albums"
    :key="album"
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
  {
    name: "Ready To Be",
    group: "Twice",
    price: "$25.99",
    img: "https://preview.redd.it/twice-the-12th-mini-album-ready-to-be-vinyl-packaging-v0-n8umb45sqwfa1.jpg?width=640&crop=smart&auto=webp&s=9f8a8ed91d42f12e47d21f4775466a60cd8cd6af",
  },
  {
    name: "Sector 17",
    group: "Seventeen",
    price: "$12.99",
    img: "https://m.media-amazon.com/images/W/IMAGERENDERING_521856-T1/images/I/71+IEJ80J2L._UF1000,1000_QL80_.jpg",
  },
  {
    name: "NewJeans 1st EP",
    group: "NewJeans",
    price: "$10.42",
    img: "https://cdn-contents.weverseshop.io/public/shop/9912453e36490a90474afaf1f6e38606.png",
  },
  {
    name: "Savage",
    group: "Aespa",
    price: "$26.65",
    img: "https://m.media-amazon.com/images/W/IMAGERENDERING_521856-T1/images/I/61RWfu-jSyL.jpg",
  },
  {
    name: "The Beginning: Cupid",
    group: "FiftyFifty",
    price: "$22.95",
    img: "http://cdn.shopify.com/s/files/1/1801/5317/products/009001022441_1200x1200.jpg?v=1677085045",
  },
  {
    name: "Face The Sun",
    group: "Seventeen",
    price: "$17.99",
    img: "https://target.scene7.com/is/image/Target/GUEST_09db1f32-9533-47bd-a703-46fb4a987ef9?wid=488&hei=488&fmt=pjpeg",
  },
  {
    name: "Fearless",
    group: "Le Sserafim",
    price: "$17.89",
    img: "https://m.media-amazon.com/images/W/IMAGERENDERING_521856-T1/images/I/41UQBn9H8lL._AC_UF894,1000_QL80_.jpg",
  },
  {
    name: "The Chaos Chapter: Freeze",
    group: "TXT",
    price: "$26.67",
    img: "https://cdn.shopify.com/s/files/1/0469/3927/5428/products/txt-album-the-chaos-chapter-freeze-weverse-gift-pre-order-149161_480x480.jpg?v=1619768741",
  },
  {
    name: "Beam Of Prism",
    group: "Viviz",
    price: "$24.99",
    img: "https://cdn.shopify.com/s/files/1/2248/9053/products/viviz_stand_807c2ee9-5a4f-4069-bb28-0530b7db2c25_1024x1024@2x.jpg?v=1644394175",
  },
  {
    name: "Love Poem",
    group: "IU",
    price: "$21.99",
    img: "https://d3tvwjfge35btc.cloudfront.net/Assets/74/294/L_p0132429474.jpeg",
  },
  {
    name: "Manifesto: Day 1",
    group: "Enhypen",
    price: "$15.90",
    img: "https://images.genius.com/74a495ca68936ba3de742bdbc8973a77.1000x1000x1.png",
  },
];
</script>

<style lang="css" scoped>
.title {
}
</style>

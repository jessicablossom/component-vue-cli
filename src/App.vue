<template>
  <div id="app">
    <Navbar title="Frutas y Verduras"></Navbar>
    <h1>Frutas y Verduras</h1>
    <p>Alumna: Jessica Francavilla</p>
    <div class="container">
      <div v-for="(item, i) in items" :key="i">
        <Tabla :item="item" v-bind:class="!item.stock ? 'dark' : ''"></Tabla>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Tabla from "./components/Tabla.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Tabla,
  },
  data() {
    return {
      items: [
        {
          name: "Palta",
          stock: true,
          price: 208,
          image:
            "https://d3ugyf2ht6aenh.cloudfront.net/stores/971/857/products/palta1-3b6ad84ee39bad581215909250506090-480-0.jpg",
        },
        {
          name: "Papa",
          stock: false,
          price: 80,
          image:
            "https://d3ugyf2ht6aenh.cloudfront.net/stores/971/857/products/papa-blanca1-6b838149e859d02f9915909261260760-480-0.jpg",
        },
        {
          name: "Ciruela",
          stock: false,
          price: 273,
          image:
            "https://d3ugyf2ht6aenh.cloudfront.net/stores/971/857/products/ciruela-roja1-380222aa0ee1c50d0315908474173303-480-0.jpg",
        },
        {
          name: "Uva Negra",
          stock: true,
          price: 499,
          image:
            "https://d3ugyf2ht6aenh.cloudfront.net/stores/971/857/products/uvared-scaled-e15876674047551-5891d743848bdd1f5f15908534528308-480-0.jpg",
        },
        {
          name: "Melon",
          stock: true,
          price: 455,
          image:
            "https://d3ugyf2ht6aenh.cloudfront.net/stores/971/857/products/melon-amarillo-x-unidad1-e7ca4a82009103f3c015947235312287-480-0.jpg",
        },
        {
          name: "Naranja",
          stock: true,
          price: 104,
          image:
            "https://d3ugyf2ht6aenh.cloudfront.net/stores/971/857/products/naranja1-2b78bc3cc3afbe01f315908524247510-480-0.jpg",
        },
        {
          name: "Pera",
          stock: true,
          price: 195,
          image:
            "https://d3ugyf2ht6aenh.cloudfront.net/stores/971/857/products/pera-11-86696614c24123138315908529229799-480-0.jpg",
        },
        {
          name: "Kiwi",
          stock: false,
          price: 324,
          image:
            "https://d3ugyf2ht6aenh.cloudfront.net/stores/971/857/products/kiwi1-5bee2b0f4cb471186e15908500798577-480-0.jpg",
        },
      ],
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Nunito&display=swap");
@import "./styles.css";

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>

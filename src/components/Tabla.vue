<template>
  <div class="element">
    <h3>{{ item.name }}</h3>
    <h3>$ {{ item.price }}</h3>
    <img :src="item.image" />
    <p v-if="item.stock">Hay stock</p>
    <p v-else>No hay stock</p>
    <button v-on:click="alert" class="btn">Agregar</button>
  </div>
</template>

<script>
export default {
  name: "tabla",
  props: ["item", "alert"],
};
</script>

<style></style>

<template>
  <div id="icecream-store">
    <h1>Icecream store</h1>

    <label>Quantity: <input type="number" v-model="quantity"></label>

    <label>Size:
      <select v-model="size">
        <option value="100">Small</option>
        <option value="150">Medium</option>
        <option value="200">Giant</option>
      </select>
    </label>

    <label>Flavour:</label>
    <label><input type="radio" v-model="flavour" name="flavour" value="#F3E5AB">Vanilla</label>
    <label><input type="radio" v-model="flavour" name="flavour" value="#5B2F00" />Chocolate</label>
    <label><input type="radio" v-model="flavour" name="flavour" value="#DE0934" />Strawberry</label>

    <label><input type="checkbox" v-model="napkin"> Napkin</label>

    <IceCreams :quantity="quantity" :flavour="flavour" :size="size" :napkin="napkin" />
  </div>
</template>

<style>label { display: block }</style>

<script setup>

import { ref } from 'vue';
import IceCreams from "./IceCreams.vue";

const quantity = ref(1);
const flavour = ref("#5B2F00");
const size = ref(150);
const napkin = ref(true);

</script>

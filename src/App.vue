<script setup>
import { ref } from 'vue';
import Hedaer from './components/Layout/Header.vue';
import Hero from './components/Hero.vue';
import AboutBrand from './components/AboutBrand.vue';
import Products from './components/Products4Column.vue'
import Ideas from './components/Ideas.vue';



</script>

<template>
  <div class="container">
    <Hedaer/>
    <Hero/>
    <AboutBrand/>
    <Products 
      :products="products"
     />
     <Ideas/>
  </div>
</template>

<style lang="scss">
@import url('https://fonts.cdnfonts.com/css/satoshi');
@import url('https://fonts.cdnfonts.com/css/clash-display');

* {
  box-sizing: border-box;
  font-weight: 400;
}
body {
  margin: 0;
  padding: 0;
  font-family: 'Satoshi', sans-serif;
  // font-family: 'Clash Display', sans-serif;
}
img {
  max-width: 100%;
}
.container {
  padding: 0 ;
  max-width: 1440px;
  margin: 0 auto;
}
</style>

<template>
  <div class="products-container">
      <div class="products">
      <Product
        v-for="product of products.splice(0, 4)"
        :key="product.id"
        :img="product.img"
        :title="product.title"
        :price="product.price"/>
    </div>
    <a href="#" class="products-link">View Collection</a>
  </div>

</template>
<script setup>
import {ref} from 'vue'
import Product from "../components/Product.vue";

const props = defineProps({
  products: {
    type: Array,
    required: true,
  },
});
const products = ref([
  {
    id: 1,
    img: '/img/product1.jpeg',  
    title: 'The Dandy chair',
    price: 250
  },
  {
    id: 2,
    img: '/img/product2.jpeg',  
    title: 'Rustic Vase Set',
    price: 155
  },
  {
    id: 3,
    img: '/img/product3.jpeg',  
    title: 'The Silky Vase',
    price: 125
  },
  {
    id: 4,
    img: '/img/product4.jpeg',  
    title: 'The Lucy Lamp',
    price: 399
  },
  {
    id: 5,
    img: '/img/product4.jpeg',  
    title: 'The Lucy Lamp',
    price: 322
  },
  {
    id: 6,
    img: '/img/product4.jpeg',  
    title: 'The Lucy Lamp',
    price: 32
  },
])
</script>

<style lang="scss">
.products {
  display: flex;
  grid-template-columns: repeat(4, 1fr);
  column-gap: 20px;
  padding: 0 80px;
  &-container {
    margin-bottom: 56px;
  }
  &-link {
    display: block;
    text-align: center;
    color: #2A254b;
    text-decoration: none;
    &:hover {
      text-decoration: underline;
    }
  }

}
</style>

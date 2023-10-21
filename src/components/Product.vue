<template>
  <div class="product">
    <a href="" class="product-image">
      <img :src="img" :alt="title" />
    </a>
    <a href="#" class="product-name">{{ title }}</a>
    <span class="product-price">£{{ price }}</span>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  img: {
    type: String,
    required: true,
  },
  title: {
    type: String,
    required: true,
  },
  price: {
    type: Number,
    required: true,
  },
});
</script>

<style lang="scss">
.product {
  &-image {
    display: flex;
    margin-bottom: 24px;
  }
  &-name {
    display: block;
    color: #2a254b;
    font-size: 20px;
    line-height: 28px;
    text-decoration: none;
    margin-bottom: 8px;
    &:hover {
      text-decoration: underline;
    }
    &-price {
      display: block;
      font-size: 18px;
      color: #2a254b;;
    }
  
  }
}
</style>

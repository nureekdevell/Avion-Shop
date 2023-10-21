<template>
    <div class="about-brand">
        <h3 class="about-brand__title">What makes our brand different</h3>
        <div class="about-brand-elements">
            <div class="about-brand-element"
            v-for="(element, i) of aboutBrands"
                :key="i">
                <img class="about-brand-element__img" 
                 :src="element.img"
                 :alt="element.title"
                 >
                <h4 class="about-brand-element__title">{{element.title}}</h4>
                <span class="about-brand-element__description">{{ element.description  }}</span>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';
const aboutBrands = [
    {
        img: '/svg/delivery.svg',
        title: 'Next day as standard',
        description: 'Order before 3pm and get your order the next day as standard',

    },
    {
        img: '/svg/checkmark.svg',
        title: 'Made by true artisans',
        description: 'Handmade crafted goods made with real passion and craftmanship',

    },
    {
        img: '/svg/purchase.svg',
        title: 'Unbeatable prices',
        description: 'For our materials and quality you won’t find better prices anywhere',

    },
    {
        img: '/svg/sprout.svg',
        title: 'Recycled packaging',
        description: 'We use 100% recycled to ensure our footprint is more manageable',

    },
]
</script>

<style lang="scss" scoped>
    .about-brand {
        padding: 80px 80px 130px 80px;
        &__title {
            text-align: center;
            font-size: 24px;
            color: #2a254b;
            margin: 0 0 84px 0;
        }
        &-elements {
            display: grid;
            grid-template-columns: repeat(4, 210px);
            justify-content: space-between;
        }
    }
</style>
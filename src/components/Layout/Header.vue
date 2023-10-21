<template>
    <header class="header">
       <div class="header-top">
        <div class="header-top-search">
            <img src="/svg/header-search.svg" alt="search">
        </div>
        <a href="#" class="header-logo">Avion</a>
        <div class="header-top-right">
            <div class="header-top-right__cart">
                <a href="#">
                    <img src="/svg/shopping-cart.svg" alt="shopping">
                </a>
            </div>

            <div class="header-top-right__profile">
                <a href="#">
                    <img src="/svg/user-avatar.svg" alt="profile">
                </a>
            </div>
        </div>
       </div> 
       <div class="header-menu">
        <a class="header-menu__link" :href="element.path" v-for="(element, i) of menu" :key="i">{{ element.name }}</a>
       </div>
    </header>
</template>

<script setup>
import { ref } from 'vue';

const menu = [
    {
        name: 'Plants pots',
        path: '/plant'
    },
    {
        name: 'Ceramics',
        path: '/ceramics'
    },
    {
        name: 'Tables',
        path: '/tables'
    },
]

</script>

<style lang="scss" scoped>
    .header {
        height: 136px;
        padding: 0 20px;
        background: #fff;
        &-top {
            display: flex;
            justify-content: space-between;
            height: 70px;
            align-items: center;
            border-bottom: 1px solid rgba(0, 0,  0, .15);
            &-right {
            display: flex;
            align-items: center;

            &__cart {
                margin-right: 16px;
            }

        }
        }
        &-logo {
            color: #222022;
            font-size: 24px;
            font-family: 'Clash Display', sans-serif;
            text-decoration: none;
            text-align: center;
            &:hover {
                text-decoration: underline;
            }
        }
        &-menu {
            height: 62px;
            display: flex;
            justify-content: center;
            align-items: center;
            &__link {
                margin: 0 22px;
                color: #726e8d;
                font-size: 16px;
                text-decoration: none;
                &:hover {
                    text-decoration: underline;
                }
            }
        }
        
    }
</style>
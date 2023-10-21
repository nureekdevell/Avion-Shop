<template>
                <div class="hero-info-text">
                <h2 class="ero-info__title">Luxury homeware for people who love timeless design quality</h2>
                <span class="hero-info__description">Shop the new Spring 2022 collection today</span>
            </div>
            <a href="#" class="hero-info-link">View collection</a>
</template>

<script setup>
    const props = defineProps({
        title: {
            type: String,
            reqiured: false,
        },
        description: {
            type: String,
            reqiured: false,
        },
        link: {
            type: String,
            reqiured: false,
        }
    })
</script>

<style lang="scss" scoped>
.hero {
    &-info {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        background-color: #fff;
        max-width: 630px;
        padding: 50px 55px;
        height: 444px;
        color: #5B5676;
        &-link {
            color: #2A254B;
            text-decoration: none;
            &:hover {
                text-decoration: underline;
            }
        }

    }
}
    
</style>
<template>
    <div class="hero">
        <div class="hero-info">
            <div class="hero-info-text">
                <h2 class="ero-info__title">Luxury homeware for people who love timeless design quality</h2>
                <span class="hero-info__description">Shop the new Spring 2022 collection today</span>
            </div>
            <a href="#" class="hero-info-link">View collection</a>

        </div>
    </div>
</template>

<script>

</script>

<style lang="scss" scoped>
.hero {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    background: url("/img/hero.png");
    height: 704px;
    background-size: cover;
    padding-right: 80px;

    &-img {
        max-width: 100%;
    }
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
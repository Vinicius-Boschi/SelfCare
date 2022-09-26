<template>
    <main class="main">
        <div class="main__banner">
            <img src="../../public/img/offer.png" alt="banner">
        </div>
        <div class="main__text">
            <h1 class="main__title">Promoção</h1>
            <p class="main__qntProducts">9 produtos</p>
        </div>
        <Products />
    </main>
</template>

<script>
    import Products from './Products.vue'

    export default {
        name: 'Main',
        components: {
            Products
        }
    }
</script>

<style lang="scss">
    @import '../assets/variables.scss';

    .main {
        
        &__banner {
            background-color: $green;
            display: flex;
            justify-content: center;
            padding: 3rem;
        }

        &__text {
            display: flex;
            justify-content: space-between;
            padding: 2rem;
        }

        &__title {
            font-weight: bold;
            font-size: 20px;
        }

        &__qntProducts {
            font-size: 18px;
        }
    }

</style>
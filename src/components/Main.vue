<template>
    <main class="main">
        <div class="main__banner">
            <img src="https://user-images.githubusercontent.com/74377158/192579977-bc1af80b-8964-4e75-aefa-2c131d9a31f0.png" alt="banner">
        </div>
        <div class="main__text">
            <h1 class="main__title">{{ title }}</h1>
            <p class="main__qntProducts"></p>
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
        },
        data() {
            return {
                title: 'Promoção'
            }
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

            img {
                @include for-phone-only {
                    width: 100%;
                }
            }
        }

        &__text {
            display: flex;
            justify-content: space-between;
            padding: 2rem;
            border-bottom: 1px solid $gray-two;
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
<template>
  <section class="main__section">
    <div class="main__products">
        <img class="main__products-img" src="../../public/img/product-1.png" alt="product-1">
        <h2 class="main__title-products">Lorem ipsum dolor sit</h2>
        <p class="main__price">R$ <span>50,00</span></p>
    </div>
    <div class="main__products">
        <img class="main__products-img" src="../../public/img/product-1.png" alt="product-1">
        <h2 class="main__title-products">Lorem ipsum dolor sit</h2>
        <p class="main__price">R$ <span>50,00</span></p>
    </div>
    <div class="main__products">
        <img class="main__products-img" src="../../public/img/product-1.png" alt="product-1">
        <h2 class="main__title-products">Lorem ipsum dolor sit</h2>
        <p class="main__price">R$ <span>50,00</span></p>
    </div>
    <div class="main__products">
        <img class="main__products-img" src="../../public/img/product-1.png" alt="product-1">
        <h2 class="main__title-products">Lorem ipsum dolor sit</h2>
        <p class="main__price">R$ <span>50,00</span></p>
    </div>
  </section>
</template>

<script>
    export default {
        name: 'Products'
    }
</script>

<style lang="scss">
    @import '../assets/variables.scss';

    .main {

        &__section {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            justify-items: center;
            padding: 2rem;
        }

        &__products-img {
            width: 100%;
            margin-bottom: 1rem;
        }

        &__price {
            margin-top: .5rem;

            span {
                color: $green-two;
            }
        }
    }

</style>
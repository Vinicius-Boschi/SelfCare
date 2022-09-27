<template>
  <header class="header">
    <div class="header__content">
        <div class="header__logo">
            <img src="../../public/img/logo.png" alt="logo">
        </div>
        <div class="header__clickable">
            <a href="#">
                <img src="../../public/img/magnifyingglass.png" alt="magnifying glass">
            </a>
            <a href="#">
                <img src="../../public/img/account.png" alt="account">
            </a>
            <a href="#">
                <img src="../../public/img/cart.png" alt="cart">
            </a>
        </div>
    </div>
  </header>
</template>

<script>
    export default {
        name: 'Header'
    }
</script>

<style lang="scss">
    @import '../assets/variables.scss';

    .header {
        padding: 2rem;

        @include for-phone-only {
            padding: 1rem;
        }

        &__content {
            display: flex;
            justify-content: space-around;
            align-items: center;
        }

        img {
            margin: 1rem;
            cursor: pointer;
        }
    }

</style>
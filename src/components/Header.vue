<template>
  <header class="header">
    <div class="header__content">
        <div class="header__logo">
            <img :src="logo" alt="logo">
        </div>
        <div class="header__clickable">
            <a v-for="item in linksHeader" :key="item.id" :href="item.link">
                <img :src="item.image" :alt="item.name">
            </a>
        </div>
    </div>
  </header>
</template>

<script>
    export default {
        name: 'Header',
        data() {
            return {
                logo: 'https://user-images.githubusercontent.com/74377158/192580024-929b3b16-b466-4ca8-a896-7f5d881a71e8.png',
                linksHeader: [
                    {link: '#', image: 'https://user-images.githubusercontent.com/74377158/192580026-a0e4e1b4-9393-41f6-830f-bff5855cf959.png', name: 'magnifying glass'},
                    {link: '#', image: 'https://user-images.githubusercontent.com/74377158/192580012-10bfa35f-c2f0-49d7-916c-8807f8690e86.png', name: 'account'},
                    {link: '#', image: 'https://user-images.githubusercontent.com/74377158/192580015-db469ed7-000d-430a-a27e-2ca850158b9b.png', name: 'cart'}
                ]
            }
        }
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
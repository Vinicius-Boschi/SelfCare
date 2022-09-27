<template>
  <section class="main__section">
    <div class="main__products" v-for="(item, index) in products" :key="item.id">
        <img class="main__products-img" :src="item.image" :alt="item.name">
        <h2 class="main__title-products">{{ index + 1 }} - {{ item.title }}</h2>
        <p class="main__price">{{ item.prefix }} <span>{{ item.price }}</span></p>
    </div>
  </section>
</template>

<script>
    export default {
        name: 'Products',
        data() {
            return {
                products: [
                    {
                        image: 'https://user-images.githubusercontent.com/74377158/192579979-65c3a167-0919-4161-b740-58c2af965b09.png', name: 'Produto 1', title: 'Lorem ipsum dolor sit', prefix: 'R$', price: '50,00'
                    },
                    {
                        image: 'https://user-images.githubusercontent.com/74377158/192579981-3eee82ec-9470-47a1-a755-90fc15a3175e.png', name: 'Produto 2', title: 'Lorem ipsum dolor sit', prefix: 'R$', price: '50,00'
                    },
                    {
                        image: 'https://user-images.githubusercontent.com/74377158/192579983-c2684d21-e84f-4b1e-8f40-20ee00cd37d9.png', name: 'Produto 3', title: 'Lorem ipsum dolor sit', prefix: 'R$', price: '50,00'
                    },
                    {
                        image: 'https://user-images.githubusercontent.com/74377158/192579986-364e5e08-8b16-4a78-8894-d5b627d5ca5a.png', name: 'Produto 4', title: 'Lorem ipsum dolor sit', prefix: 'R$', price: '50,00'
                    },
                    {
                        image: 'https://user-images.githubusercontent.com/74377158/192579988-d4d60897-e2d2-453a-97da-4738361e0798.png', name: 'Produto 5', title: 'Lorem ipsum dolor sit', prefix: 'R$', price: '50,00'
                    },
                    {
                        image: 'https://user-images.githubusercontent.com/74377158/192579991-e4a2a21a-e9aa-4c10-90e9-affe66f2623d.png', name: 'Produto 6', title: 'Lorem ipsum dolor sit', prefix: 'R$', price: '50,00'
                    },
                    {
                        image: 'https://user-images.githubusercontent.com/74377158/192579992-fd87ca4e-72ed-41a7-a905-74a30beb4e72.png', name: 'Produto 7', title: 'Lorem ipsum dolor sit', prefix: 'R$', price: '50,00'
                    },
                    {
                        image: 'https://user-images.githubusercontent.com/74377158/192580000-37294d9b-16e5-4698-8242-45a8700e6bb4.png', name: 'Produto 8', title: 'Lorem ipsum dolor sit', prefix: 'R$', price: '50,00'
                    },
                    {
                        image: 'https://user-images.githubusercontent.com/74377158/192580004-96c25b81-3099-4ee2-b4c3-fd94a9a87c26.png', name: 'Produto 9', title: 'Lorem ipsum dolor sit', prefix: 'R$', price: '50,00'
                    },
                ],
            }
        },
        mounted() {
            let products = document.querySelectorAll('.main__products').length
            let qnt = document.querySelector('.main__qntProducts')
            qnt.innerHTML = products + ' produtos'
        }
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
            gap: 2rem;

            @include for-phone-only {
                grid-template-columns: repeat(2, 1fr);
            }
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
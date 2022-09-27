<template>
    <footer class="footer">
        <div class="footer__list">
            <ul>
                <li v-for="link in links" :key="link.id">
                    <a class="footer__link" :href="link.link">{{ link.name }}</a>
                </li>
            </ul>
            <div class="footer__contact">
                <label for="#" class="footer__label">{{ labelName }}</label>
                <input class="footer__input" type="email" name="email" id="email" placeholder="Digite seu melhor email">
                <button class="footer__button">{{ buttonName }}</button>
            </div>
        </div>
        <div class="footer__info">
            <div class="footer__media">
                <img :src="instagram" alt="">
                <img :src="facebook" alt="facebook">
            </div>
            <div class="footer__payment">
                <img :src="mastercard" alt="mastercard">
                <img :src="paypal" alt="paypal">
                <img :src="visa" alt="visa">
            </div>
        </div>
    </footer>
</template>

<script>
    export default {
        name: 'Footer',
        data() {
            return {
                labelName: 'Newsletter',
                buttonName: 'Inscrever',
                instagram: 'https://user-images.githubusercontent.com/74377158/192580021-4f0d79cc-994d-493d-b091-530d73ee34f0.png',
                facebook: 'https://user-images.githubusercontent.com/74377158/192580017-b548e25d-73fa-4ec0-b12b-a4b035790edf.png',
                mastercard: 'https://user-images.githubusercontent.com/74377158/192579975-1b6c4432-a4da-4a0e-9b3a-b1812ba69a9a.png',
                paypal: 'https://user-images.githubusercontent.com/74377158/192579978-2c5f0355-7409-405c-b107-2ff42ba44300.png',
                visa: 'https://user-images.githubusercontent.com/74377158/192580009-85995951-d18c-485b-8a18-215d8ff5009f.png',
                links: [
                    {link: '#', name:'Contato'},
                    {link: '#', name:'Termos de Serviço'},
                    {link: '#', name:'Política de Privacidade'},
                    {link: '#', name:'Cancelamento, troca e reembolso'}
                ]
            }
        }
    }
</script>

<style lang="scss">
    @import '../assets/variables.scss';

    .footer {
        background-color: $white;
        padding: 2rem;
        border-top: 1px solid $gray-two;

        &__list {
            display: flex;
            justify-content: space-around;
            line-height: 2;

            @include for-phone-only {
                flex-direction: column;
            }
        }

        &__link {
            text-decoration: none;
            color: inherit;
        }

        &__label {
            display: flex;
            line-height: 2;
            font-weight: bold;
        }

        &__input {
            margin-right: 1rem;
            padding: .5rem;
        }

        &__button {
            border: none;
            background-color: $green-two;
            color: $white;
            padding: .8rem;
            cursor: pointer;
        }

        &__info {
            display: flex;
            justify-content: space-around;
            align-items: center;
            margin-top: 2rem;
            border-top: 1px solid $gray-two;
            padding: 0.5rem;
        }

        &__media {
            margin-left: -4rem;

            @include for-phone-only {
                margin: 0 auto;
            }
        }

        &__media, &__payment {

            img {
                margin-right: 1rem;
            }
        }
    }

</style>
<template>
    <footer class="footer">
        <div class="footer__list">
            <ul>
                <li>
                    <a class="footer__link" href="#">Contato</a>
                </li>
                <li>
                    <a class="footer__link" href="#">Termos de Serviço</a>
                </li>
                <li>
                    <a class="footer__link" href="#">Política de Privacidade</a>
                </li>
                <li>
                    <a class="footer__link" href="#">Cancelamento, troca e reembolso</a>
                </li>
            </ul>
            <div class="footer__contact">
                <label for="#" class="footer__label">Newsletter</label>
                <input class="footer__input" type="email" name="email" id="email" placeholder="Digite seu melhor email">
                <button class="footer__button">Inscrever</button>
            </div>
        </div>
        <div class="footer__info">
            <div class="footer__media">
                <img src="../../public/img/instagram.png" alt="instagram">
                <img src="../../public/img/facebook.png" alt="facebook">
            </div>
            <div class="footer__payment">
                <img src="../../public/img/mastercard.png" alt="mastercard">
                <img src="../../public/img/paypal.png" alt="paypal">
                <img src="../../public/img/visa.png" alt="visa">
            </div>
        </div>
    </footer>
</template>

<script>
    export default {
        name: 'Footer'
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
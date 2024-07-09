<template>
    <footer class="Footer">
        <div class="Footer__container">
            <h3 class="Footer__title">
                Контакти
            </h3>
            <div class="Footer__socials">
                <a href="#" class="Footer__socials-item">
                    <img src="../../assets/images/logos/person-logo.svg" alt="person-logo">
                </a>
                <a href="#" class="Footer__socials-item">
                    <img src="../../assets/images/logos/behance-logo.svg" alt="behance-logo">
                </a>
                <a href="#" class="Footer__socials-item">
                    <img src="../../assets/images/logos/telegram-logo.svg" alt="telegram-logo">
                </a>
                <a href="#" class="Footer__socials-item">
                    <img src="../../assets/images/logos/instagram-logo.svg" alt="instagram-logo">
                </a>
                <a href="#" class="Footer__socials-item">
                    <img src="../../assets/images/logos/gmail-logo.svg" alt="gmail logo">
                </a>
            </div>
            <div class="Footer__bottom">
                <p class="Footer__bottom-text">© 2023-..., Complex Agency - example@gmail.com</p>
                <p class="Footer__bottom-policy">Політика сайту та обробка персональних даних</p>
            </div>
        </div>
    </footer>
</template>

<script setup>

</script>

<style lang="scss" scoped>
.Footer {
    margin-top: 40px;

    &__container {
        max-width: 815px;
        margin: 40px auto 0;
    }

    &__title {
        font-weight: 700;
        font-size: 96px;
        line-height: 116px;
        letter-spacing: 0.02em;
        position: relative;
        text-align: center;
        width: fit-content;
        margin: 0 auto;

        &:after {
            content: "";
            background-image: url('../../assets/images/stars-top.svg');
            background-repeat: no-repeat;
            background-size: 100%;
            width: 42px;
            height: 62px;
            position: absolute;
            right: -10%;
            top: 0;

        }

        &:before {
            content: "";
            background-image: url('../../assets/images/stars-bottom.svg');
            background-repeat: no-repeat;
            background-size: 100%;
            width: 59px;
            height: 62px;
            position: absolute;
            left: -10%;
            bottom: -10%;
        }
    }

    &__socials {
        margin-top: 40px;
        display: flex;
        justify-content: center;
        gap: 40px;

        &-item {
            width: 110px;
            height: 110px;
            background: #fff;
            border-radius: 50%;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: transform 250ms ease-in-out;

            &:after {
                content: "";
                width: 130px;
                height: 130px;
                position: absolute;
                top: -10px;
                left: -10px;
                border: 1px solid #4e4e4e;
                border-radius: 50%;
            }

            &:hover {
                background: radial-gradient(circle at 49.29% 50.71%, #2EECC5 0%, #00644F 100%);
                transform: scale(1.25);
            }
        }

    }

    &__bottom {
        margin: 40px auto;
        width: 100%;

        &-text {
            font-weight: 400;
            font-size: 15px;
            line-height: 105.6%;
            text-align: center;
            color: rgba(255, 255, 255, 0.7);
        }

        &-policy {
            font-weight: 400;
            font-size: 13px;
            line-height: 105.6%;
            text-align: center;
            color: rgba(255, 255, 255, 0.4);
            margin-top: 18px;
        }
    }
}
</style>
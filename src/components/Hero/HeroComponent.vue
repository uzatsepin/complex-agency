<template>
    <div class="hero">
        <div class="hero__container">
            <Header />

            <div class="hero__text">
                <h1 class="hero__title">Комплексні рішення для твого бізнесу</h1>
                <p class="hero__descr">
                    Ми - агенство цифрових рішень під ключ, від дизайну до розробки, ми виконаємо
                    твое побажання.
                </p>
                <div class="hero__text-bottom">
                    <PrimaryButton class="hero__text-bottom-button">
                        Детальніше
                        <Icon icon="iconamoon:arrow-right-2" width="24" height="24" />
                    </PrimaryButton>
                    <a class="hero__text-bottom-link" href="#"> Залишились запитання? </a>
                </div>
            </div>

            <div class="hero__expert"></div>
        </div>
    </div>
</template>

<script setup>
import PrimaryButton from "../Others/PrimaryButton.vue"
import Header from "./Header.vue"
import { Icon } from "@iconify/vue"
</script>

<style lang="scss" scoped>
.hero {
    height: 100vh;
    position: relative;

    &::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-image: url("../../assets/images/hero-bg.svg");
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        background-color: rbga(#180b1c, 0.04);
        mix-blend-mode: luminosity;
        height: 100vh;
        z-index: 1;
    }

    &::after {
        content: "";
        position: absolute;
        width: 100%;
        height: 5px;
        left: 0px;
        bottom: 0;
        background: linear-gradient(90deg,
                rgba(42, 188, 158, 0) 0%,
                #2abc9e 48.65%,
                rgba(42, 188, 158, 0) 100%);
    }

    &__container {
        max-width: 1305px;
        margin: 0 auto;
    }

    &__text {
        margin-top: 200px;
        max-width: 690px;
        position: relative;
        z-index: 2;

        &-bottom {
            margin-top: 84px;
            display: flex;
            align-items: center;

            &-link {
                font-weight: 400;
                font-size: 19px;
                line-height: 23px;
                color: rgba(255, 255, 255, 0.4);
                margin-left: 24px;
                transition: all 250ms ease-in-out;

                &:hover {
                    color: rgba(255, 255, 255, 0.8);
                    cursor: pointer;
                }
            }

            &-button {
                padding: 17px 37px;
            }
        }
    }

    &__title {
        font-weight: 800;
        font-size: 65px;
        line-height: 79px;
        background: linear-gradient(91.2deg, #b5feef 10.31%, #2eecc5 165.09%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
        text-fill-color: transparent;

        & p {
            font-size: 45px;
            line-height: 54px;
        }
    }

    &__descr {
        margin-top: 30px;
        font-weight: 500;
        font-size: 22px;
        line-height: 27px;
        color: rgba(255, 255, 255, 0.65);
    }

    &__expert {
        background-image: url("../../assets/images/expert-image.png");
        background-repeat: no-repeat;
        background-size: cover;
        width: 770px;
        height: 809px;
        position: absolute;
        bottom: 0;
        right: 0;
    }
}
</style>

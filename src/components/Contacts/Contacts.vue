<template>
    <div class="Contacts">
        <div class="Contacts__container">
            <div class="Contacts__title">
                Залишити заявку
            </div>

            <form class="Contacts__form">
                <div class="Contacts__form-left">
                    <div class="Contacts__form-name">
                        <label class="Contacts__form-label" for="name">Ваше ФІО</label>
                        <input class="Contacts__form-input" type="text" id="name" placeholder="Іван"
                            v-model="formData.name">
                    </div>
                    <div class="Contacts__form-phone">
                        <label class="Contacts__form-label" for="phone">Ваш номер телефона</label>
                        <input class="Contacts__form-input" type="phone" id="phone" placeholder="+380..."
                            v-model="formData.phone">
                    </div>
                    <div class="Contacts__form-direction">
                        <label class="Contacts__form-label" for="direction">Напрямок</label>
                        <input class="Contacts__form-input" type="text" id="direction"
                            placeholder="Дизайн/Розбробка/..." v-model="formData.direction">
                    </div>
                </div>
                <div class="Contacts__form-right">
                    <div class="Contacts__form-email">
                        <label class="Contacts__form-label" for="email">Поштова скринька/Telegram</label>
                        <input class="Contacts__form-input" type="text" id="email" placeholder="Дизайн/Розбробка/..."
                            v-model="formData.email">
                    </div>
                    <div class="Contacts__form-tech">
                        <label class="Contacts__form-label" for="techTask">Технічне завдання (за наявності)</label>
                        <input class="Contacts__form-input" type="text" id="techTask"
                            placeholder="Потрібно зробити сайт з використанням Vue.js...." v-model="formData.tech">
                    </div>
                    <button class="Contacts__form-button button">
                        Надіслати
                        <Icon icon="lucide:send" />
                    </button>
                </div>
            </form>

            <div class="Contacts__wrapper">
                <img src="../../assets/images/phone-img.png" alt="Phone Img">
            </div>
        </div>
    </div>
</template>

<script setup>
import { Icon } from '@iconify/vue';
import { reactive } from 'vue'

const formData = reactive({
    name: '',
    phone: '',
    direction: '',
    email: '',
    tech: ''
})

</script>

<style lang="scss" scoped>
.Contacts {
    margin-top: 200px;
    background: linear-gradient(91.69deg, #313134 -11.81%, #222224 23.9%, #12473C 60.63%, #292929 110.44%);
    border: 1px solid rgba(255, 255, 255, 0.2);

    &__container {
        max-width: 1410px;
        margin: 0 auto;
        padding: 45px 0 47px;
        position: relative;
    }

    &__title {
        font-weight: 700;
        font-size: 50px;
        line-height: 110.6%;
        background: linear-gradient(91.2deg, #B5FEEF 10.31%, #2EECC5 165.09%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
        text-fill-color: transparent;
        text-shadow: 0px 0px 36px rgba(165, 252, 235, 0.2);
    }

    &__wrapper {
        position: absolute;
        right: 0;
        bottom: -11%;
        overflow: hidden;

        & img {
            width: 531px;
            height: 529px;
        }
    }

    &__form {
        max-width: 922px;
        margin-top: 20px;
        display: flex;
        gap: 48px;

        &-name,
        &-phone,
        &-direction,
        &-email,
        &-tech {
            display: flex;
            flex-direction: column;
        }

        &-label {
            font-weight: 500;
            font-size: 14px;
            line-height: 153.8%;
            color: rgba(255, 255, 255, 0.7);
        }

        &-left,
        &-right {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        &-input {
            width: 437px;
            background: rgba(255, 255, 255, 0.1);
            border: 1.5px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0px 0px 38px rgba(255, 255, 255, 0.05);
            border-radius: 41px;
            padding: 13px 15px;
            transition: all 250ms ease-in-out;
            color: #FFF;
            margin-top: 4px;

            &:hover {
                cursor: pointer;
                border: 1.5px solid #2eecc5;
            }

            &:active {
                border: 1.5px solid #2eecc5;
            }

            &:focus {
                border: 1.5px solid #2eecc5;
                outline: none;
                box-shadow: 0px 0px 38px #2eecc66c;
            }
        }

        &-button {
            filter: drop-shadow(0px 0px 62px rgba(46, 236, 197, 0.15));
            background-color: rgba(46, 236, 197, 0.1);
            border: 1.5px solid #2eecc5;
            border-radius: 49px;
            font-weight: 500;
            font-size: 17px;
            line-height: 26px;
            color: #ffffff;
            border: 1px solid #2eecc5;
            padding: 13px 44px;
            transition: background-color 250ms ease-in-out;
            display: flex;
            gap: 8px;
            align-items: center;
            width: fit-content;
            margin-top: auto;

            &:hover {
                background-color: rgba(46, 236, 197, 0.4);
                cursor: pointer;
            }
        }
    }
}
</style>
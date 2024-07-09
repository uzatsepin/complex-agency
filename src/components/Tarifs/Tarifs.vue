<template>
    <section class="Tarifs">
        <div class="Tarifs__container">
            <h2 class="Tarifs__title">Тарифи</h2>

            <div class="Tarifs__carousel">
                <swiper :modules="modules" :loop="true"
                    :navigation="{ nextEl: '.arrow-right-tarifs', prevEl: '.arrow-left-tarifs' }" :slides-per-view="3"
                    :space-between="32" @swiper="onSwiper" @slideChange="onSlideChange" effect="coverflow"
                    :coverflowEffect="{
                        depth: 50,
                        modifier: 0.8,
                        rotate: 30,
                        scale: 0.8,
                        slideShadows: false,
                    }">
                    <swiper-slide v-for="tarif in tarifs" :key="tarif.id">
                        <TarifsItem :tarif="tarif" />
                    </swiper-slide>
                </swiper>
                <span class="arrow-left-tarifs arrow"></span>
                <span class="arrow-right-tarifs arrow"></span>
            </div>
        </div>
    </section>
</template>

<script setup>
import TarifsItem from './TarifsItem.vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Navigation, EffectCoverflow } from 'swiper/modules'
import 'swiper/css'
import 'swiper/swiper-bundle.css'

const modules = [Navigation, EffectCoverflow]

const tarifs = [
    {
        id: 1,
        title: "Сайт “Візитка”",
        descr: "Розробка цільових сторінок, оптимізованих для конверсій, з фокусом на залучення й утримання клієнтів, поліпшення користувацького досвіду і досягнення конкретних бізнес-цілей.",
        price: "Від 900₴",
        duration: "Від 1 дня"
    },
    {
        id: 2,
        title: "Розробка ПЗ",
        descr: "Розробка програмного забезпечення, орієнтованого на ваші бізнес-потреби, з акцентом на ефективність, безпеку та масштабованість. Наша команда забезпечує високий рівень якості та адаптацію під конкретні цілі вашого підприємства.",
        price: "Від 1400₴",
        duration: "Від 2 днів"
    },
    {
        id: 3,
        title: "Дизайн",
        descr: "Створення візуальних рішень для вашого бізнесу: від графічного дизайну та ілюстрацій до UX/UI-дизайну, забезпечуючи привабливість і зручність використання ваших продуктів.",
        price: "Від 650₴",
        duration: "Від 1 дня"
    },
    {
        id: 4,
        title: "Брендинг",
        descr: "Розробка брендингу, спрямованого на створення унікального і впізнаваного образу вашого бізнесу. Ми допомагаємо формувати стратегію бренду, що підвищує впізнаваність, довіру та лояльність клієнтів, забезпечуючи вашому бізнесу конкурентні переваги.",
        price: "Від 1200₴",
        duration: "Від 2 днів"
    },
    {
        id: 5,
        title: "Моушн-дизайн",
        descr: "Розробка моушн-дизайну, що привертає увагу та підсилює ваш бренд. Ми створюємо анімації, які ефективно комунікують ваші ідеї, підвищують залученість і залишають незабутнє враження на вашій аудиторії.",
        price: "Від 1400₴",
        duration: "Від 2 днів"
    },
    {
        id: 6,
        title: "Маркетинг",
        descr: "Розробка маркетингових стратегій, спрямованих на зростання вашого бізнесу. Ми створюємо ефективні кампанії, які підвищують впізнаваність бренду, залучають нових клієнтів і збільшують продажі, забезпечуючи стійкий розвиток вашої компанії.",
        price: "Від 10%",
        duration: "Від 3 днів"
    },
    {
        id: 7,
        title: "Телеграм боти",
        descr: "Розробка телеграм ботів, адаптованих під ваші бізнес-потреби. Ми створюємо інтелектуальних ботів, які автоматизують процеси, підвищують ефективність взаємодії з клієнтами і покращують користувацький досвід. Наші рішення забезпечують швидке реагування на запити, підвищують залученість і сприяють досягненню ваших бізнес-цілей.",
        price: "Від 800₴",
        duration: "Від 2 днів"
    }
]

</script>

<style lang="scss" scoped>
.Tarifs {
    margin-top: 20px;

    &__container {
        max-width: 1175px;
        margin: 0 auto;
    }

    &__title {
        font-weight: 700;
        font-size: 55px;
        background: linear-gradient(87.77deg, #B5FEEF 10.96%, #2EECC5 259.77%);
        -webkit-background-clip: text;
        line-height: 110.6%;
        -webkit-text-fill-color: transparent;
        background-clip: text;
        text-fill-color: transparent;
        text-shadow: 0px 0px 36px rgba(165, 252, 235, 0.2);
        text-align: center;
    }

    &__carousel {
        width: 100%;
        margin-top: 40px;
        position: relative;

        .arrow-left-tarifs,
        .arrow-right-tarifs {
            background-image: url('../../assets/images/arrow-left.svg');
            background-repeat: no-repeat;
            background-position: center;
            background-color: #282828;
            border: 1.5px solid rgba(46, 236, 197, 0.5);
            border-radius: 49px;
            width: 75px;
            height: 75px;
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            left: -20px;
            z-index: 1;
            transition: box-shadow 250ms ease-in-out;

            &:hover {
                box-shadow: 0px 0px 106px rgba(46, 236, 197, 0.5);
                cursor: pointer;
            }
        }

        .arrow-right-tarifs {
            right: -20px;
            left: unset;
            transform: translateY(-50%) rotate(180deg);
            z-index: 2;
        }
    }
}
</style>
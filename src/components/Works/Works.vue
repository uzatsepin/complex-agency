<template>
    <section class="works">
        <div class="works__container">
            <div class="works__wrapper">
                <div class="works__text">
                    <div class="works__text-title">Останні роботи</div>
                    <div class="works__text-descr">Останні кейси виконані нашими фахівцями.</div>
                    <PrimaryButton class="works__text-button">Замовити подібний проєкт</PrimaryButton>
                </div>

                <div class="works__carousel">
                    <swiper :modules="modules" :loop="true"
                        :navigation="{ nextEl: '.arrow-right', prevEl: '.arrow-left' }" :slides-per-view="1.5"
                        :space-between="100" @swiper="onSwiper" @slideChange="onSlideChange">
                        <swiper-slide v-for="slide in slides" :key="slide.id">
                            <img class="works__carousel-img" :src="slide.src" :alt="slide.alt">
                        </swiper-slide>
                    </swiper>
                    <span class="arrow-left arrow"></span>
                    <span class="arrow-right arrow"></span>
                </div>

            </div>
        </div>
    </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Navigation } from 'swiper/modules'
import 'swiper/css'
import 'swiper/swiper-bundle.css'
import PrimaryButton from "../Others/PrimaryButton.vue"

import blogImage from '@/assets/images/works/blog.png'
import sprintTech from '@/assets/images/works/spintech.png'
import phoenixAuto from '@/assets/images/works/pheonix-auto.png'
import starLab from '@/assets/images/works/star-lab.png'
import locksmitch from '@/assets/images/works/locksmitch.png'
import marketMaking from '@/assets/images/works/market-making.png'
import trainingImage from '@/assets/images/works/training.png'



const modules = [Navigation]


const slides = [
    {
        id: 1,
        alt: 'Blog page',
        src: blogImage
    },
    {
        id: 2,
        alt: 'Sprint Tech WebSite',
        src: sprintTech
    },
    {
        id: 3,
        alt: 'WebSite for Auto Thematic',
        src: phoenixAuto
    },
    {
        id: 4,
        alt: 'Star Lab website',
        src: starLab
    },
    {
        id: 5,
        alt: 'Lock Smith Visit card',
        src: locksmitch
    },
    {
        id: 6,
        alt: 'Market Making Styling',
        src: trainingImage
    },
    {
        id: 7,
        alt: 'Training buklette',
        src: marketMaking
    }
]

</script>

<style lang="scss" scoped>
.works {
    height: 100vh;
    position: relative;

    &::before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-image: url("../../assets/images/works-waves.svg");
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        background-color: rbga(#180b1c, 0.04);
        mix-blend-mode: luminosity;
        z-index: 1;
    }

    &__container {
        max-width: 1240px;
        margin: 180px auto 0;
        z-index: 3;
        position: relative;
    }

    &__wrapper {
        display: grid;
        grid-template-columns: 560px 924px;
    }

    &__carousel {
        position: relative;

        .arrow-left,
        .arrow-right {
            background-image: url('../../assets/images/arrow-left.svg');
            background-repeat: no-repeat;
            background-position: center;
            background-color: #153630;
            border: 1.5px solid rgba(46, 236, 197, 0.5);
            border-radius: 49px;
            width: 75px;
            height: 75px;
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            left: -35px;
            z-index: 1;
            transition: box-shadow 250ms ease-in-out;

            &:hover {
                box-shadow: 0px 0px 106px rgba(46, 236, 197, 0.5);
                cursor: pointer;
            }
        }

        .arrow-right {
            right: 33%;
            left: unset;
            transform: translateY(-50%) rotate(180deg);
        }

        &-img {
            border-radius: 5px;
            overflow: hidden;
            border: 1px solid #2A8B78;
        }
    }

    &__text {
        min-width: 562px;

        &-title {
            font-weight: 700;
            font-size: 55px;
            line-height: 110.6%;
            background: linear-gradient(91.2deg, #B5FEEF 10.31%, #2EECC5 165.09%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-fill-color: transparent;
            text-shadow: 0px 0px 36px rgba(165, 252, 235, 0.2);
        }

        &-descr {
            margin-top: 18px;
            font-weight: 500;
            font-size: 17px;
            line-height: 153.8%;
            color: rgba(255, 255, 255, 0.65);
        }

        &-button {
            margin-top: 57px;
            padding: 14px 20px;
        }
    }
}
</style>

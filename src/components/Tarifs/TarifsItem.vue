<template>
    <div class="TarifsItem">
        <h3 class="TarifsItem__title">
            {{ tarif.title }}
        </h3>
        <p class="TarifsItem__descr">
            {{ tarif.descr }}
        </p>

        <div class="TarifsItem__bottom">
            <div class="TarifsItem__bottom-price">{{ tarif.price }}<span>{{ tarif.duration }}</span></div>
            <PrimaryButton class="TarifsItem__bottom-button">
                Детальніше
                <Icon icon="iconamoon:arrow-right-2" width="24" height="24" />
            </PrimaryButton>
        </div>
    </div>
</template>

<script setup>
import PrimaryButton from '@/components/Others/PrimaryButton.vue'
import { Icon } from "@iconify/vue"

defineProps({
    tarif: {
        type: Object,
        required: true,
    }
})
</script>

<style lang="scss" scoped>
.TarifsItem {
    padding: 44px 24px 24px 24px;
    background: linear-gradient(168.64deg, #313134 9.31%, #292929 61.88%, #282828 111.76%);
    border: 1px solid rgba(255, 255, 255, 0.2);
    border-radius: 36px;
    height: 570px;
    width: 370px;
    display: flex;
    flex-direction: column;
    overflow: hidden;

    &__title {
        font-weight: 700;
        font-size: 32px;
        line-height: 39px;
        text-align: center;
    }

    &__descr {
        font-weight: 500;
        font-size: 17px;
        line-height: 153.8%;
        text-align: center;
        color: rgba(255, 255, 255, 0.75);
        margin-top: 50px;
    }

    &__bottom {
        margin-top: auto;
        display: flex;
        align-items: center;
        justify-content: space-between;

        &-button {
            padding: 14px 18px;
            font-size: 17px;
            font-weight: 600;
            font-size: 17px;
            line-height: 21px;
        }

        &-price {
            font-weight: 700;
            font-size: 22px;
            line-height: 153.8%;

            & span {
                display: block;
                font-weight: 500;
                font-size: 17px;
                line-height: 153.8%;
                text-align: center;
                color: rgba(255, 255, 255, 0.4);
            }
        }
    }

}
</style>
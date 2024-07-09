<template>
    <div class="WhyCard" :class="{ active }">
        <div class="WhyCard__title">{{ item.title }}</div>
        <div class="WhyCard__descr">{{ item.descr }}</div>
        <img class="WhyCard__icon" :src="item.img" />
    </div>
</template>

<script setup>
defineProps({
    item: {
        type: Object,
        required: true,
    },
    active: {
        type: Boolean,
        default: false,
    },
})
</script>

<style lang="scss" scoped>
.WhyCard {
    display: flex;
    flex-direction: column;
    gap: 17px;
    background: linear-gradient(139.56deg, #303134 10.06%, #282828 53.72%, #282828 88%);
    border: 1px solid #3b3b3b;
    position: relative;
    padding: 40px;
    width: 400px;
    height: 400px;

    &.active {
        background: linear-gradient(139.56deg, #527791 10.06%, #325597 53.72%, #193895 88%);
        border: unset;
    }

    &__title {
        font-weight: 600;
        font-size: 26px;
        line-height: 123.1%;
    }

    &__descr {
        font-weight: 500;
        font-size: 17px;
        line-height: 123.1%;
        color: rgba(255, 255, 255, 0.9);
    }

    &__icon {
        position: absolute;
        bottom: 0;
        right: 0;
    }
}
</style>

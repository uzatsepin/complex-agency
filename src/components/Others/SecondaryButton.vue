<template>
    <button class="SecondaryButton">
        <slot />
    </button>
</template>

<script setup></script>

<style lang="scss" scoped>
.SecondaryButton {
    position: relative;
    display: inline-block;
    background: #161617;
    border: 1.5px solid #2eecc5;
    box-shadow: 0px 0px 38px rgba(46, 236, 197, 0.2);
    border-radius: 4px;
    padding: 16px 43px;
    font-weight: 600;
    font-size: 19px;
    line-height: 23px;
    color: #ffffff;

    &:before {
        content: "";
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        border: 1.5px solid #2eecc5;
        border-radius: 4px;
        transition: transform 0.3s ease, opacity 0.3s ease;
        transform: translate(0, 0);
        opacity: 0;
        z-index: -1;
    }

    &:hover:before {
        transform: translate(9px, 11px);
        opacity: 0.4;
    }

    &:hover {
        cursor: pointer;
    }
}
</style>

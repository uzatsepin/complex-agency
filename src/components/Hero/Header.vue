<template>
    <header class='header'>
        <div class='header__container'>
            <div class='header__logo'>
                <img src='../../assets/images/logo.svg' alt='logo' width="131" height="65" />
            </div>
            <nav class='header__nav'>
                <ul class='header__nav-items'>
                    <li class='header__nav-list'>
                        <a href='#main' class='header__nav-link'>
                            Головна
                        </a>
                    </li>
                    <li class='header__nav-list'>
                        <a href='#whyUs' class='header__nav-link'>
                            Чому саме ми?
                        </a>
                    </li>
                    <li class='header__nav-list'>
                        <a href='#contacts' class='header__nav-link'>
                            Контакти
                        </a>
                    </li>
                </ul>
            </nav>
            <div class='header__button'>
                <PrimaryButton>
                    Замовити
                </PrimaryButton>
            </div>
        </div>
    </header>
</template>

<script setup>
import PrimaryButton from "../Others/PrimaryButton.vue"


</script>

<style lang="scss" scoped>
.header {
    padding-top: 48px;
    position: relative;
    z-index: 3;

    &__container {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    &__nav {
        &-items {
            display: flex;
            gap: 40px;
            align-items: center;
        }

        &-link {
            font-family: 'Inter', sans-serif;
            font-weight: 600;
            font-size: 20px;
            line-height: 24px;
            position: relative;
            transition: all 250ms ease-in-out;

            &::before {
                content: '';
                position: absolute;
                top: 0;
                left: 50%;
                transform: translateX(-50%);
                width: 85px;
                height: 16px;
                background-color: #2ce8c2;
                box-shadow: 0px 0px 21px rgba(44, 232, 194, 0.35);
                border-radius: 8px;
                opacity: 0;
                transition: all 200ms ease-in-out;
            }

            &:hover::before {
                opacity: 1;
                top: -75px;
            }
        }
    }
}
</style>
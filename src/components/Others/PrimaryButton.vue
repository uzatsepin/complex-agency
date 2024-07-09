<template>
    <button class="PrimaryButton">
        <slot />
    </button>
</template>

<script setup></script>

<style lang="scss" scoped>
.PrimaryButton {
    filter: drop-shadow(0px 0px 62px rgba(46, 236, 197, 0.15));
    background-color: rgba(46, 236, 197, 0.1);
    border: 1.5px solid #2eecc5;
    border-radius: 49px;
    font-weight: 600;
    font-size: 20px;
    line-height: 24px;
    color: #ffffff;
    border: 1px solid #2eecc5;
    padding: 17px 60px;
    transition: background-color 250ms ease-in-out;
    display: flex;
    gap: 8px;
    align-items: center;

    &:hover {
        background-color: rgba(46, 236, 197, 0.4);
        cursor: pointer;
    }
}

// .PrimaryButton {
// 	position: relative;
// 	display: inline-flex;
// 	width: 100%;
// 	max-width: 300px; // Ограничьте максимальную ширину кнопки
// 	overflow: hidden;
// 	border-radius: 49px;
// 	padding: 1.5px;
// 	outline: none;

// 	&-content {
// 		display: inline-flex;
// 		height: 100%;
// 		width: 100%;
// 		cursor: pointer;
// 		align-items: center;
// 		justify-content: center;
// 		border-radius: 49px;
// 		background: #2eecc60a; // Фон кнопки
// 		padding: 10px 59px;
// 		font-size: 20px;
// 		font-weight: 600;
// 		color: #ffffff;
// 		backdrop-filter: blur(30px);
// 		position: relative; // Для правильного размещения содержимого
// 		z-index: 1; // Установите z-index для верхнего слоя
// 	}

// 	&-border {
// 		position: absolute;
// 		top: 0;
// 		left: 0;
// 		right: 0;
// 		bottom: 0;
// 		border-radius: 49px;
// 		background: conic-gradient(from 90deg at 50% 50%, #b4f8ea 0%, #82fae2 50%, #2eecc5 100%);
// 		animation: spin 2s linear infinite;
// 		z-index: 0; // Установите z-index для нижнего слоя
// 		content: '';
// 		clip-path: inset(0 round 49px); // Обрежьте псевдоэлемент по границе кнопки
// 	}

// 	@keyframes spin {
// 		from {
// 			transform: rotate(0deg);
// 		}
// 		to {
// 			transform: rotate(360deg);
// 		}
// 	}
// }</style>

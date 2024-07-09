<template>
	<div class="why">
		<div class="why__container">
			<div class="why__top">
				<div class="why__text">
					<h2 class="why__title">Чому саме ми?</h2>
					<p class="why__descr">
						Ми – агенція, що спеціалізується на моушн-дизайні, розробці, лендінгах,
						брендингу та дизайні. Використовуємо комплексні бізнес-рішення. З нами ваш
						бізнес досягне нових висот.
						<span>Перегляньте наше портфоліо - воно говорить саме за себе.</span>
					</p>

					<div class="why__button">
						<SecondaryButton> Портфоліо </SecondaryButton>
					</div>
				</div>

				<WhyCard :item="cards[0]" :active="true" />
			</div>
			<div class="why__bottom">
				<WhyCard v-for="card in cards.slice(1, 4)" :key="card.id" :item="card" />
			</div>
		</div>
	</div>
</template>

<script setup>
import SecondaryButton from "../Others/SecondaryButton.vue"
import WhyCard from "./WhyCard.vue"
import moneyIcon from "@/assets/images/money-icon.svg"
import personIcon from "@/assets/images/person-icon.svg"
import timeIcon from "@/assets/images/time-icon.svg"
import supportIcon from "@/assets/images/support-icon.svg"

const cards = [
	{
		id: 1,
		title: "Адаптація під ваши потреби",
		descr:
			"Ми ретельно вивчаємо ваші потреби та цілі, щоб розробити персоналізоване рішення, яке ідеально відповідає вашим очікуванням.",
		img: moneyIcon,
		imgSize: [211, 211],
	},
	{
		id: 2,
		title: "Контроль вашого проекту",
		descr:
			"Забезпечуємо повний контроль над усіма етапами проекту, від планування до виконання, гарантуючи високу якість та своєчасне завершення.",
		img: timeIcon,
		imgSize: [200, 189],
	},
	{
		id: 3,
		title: "Команда спеціалістів",
		descr:
			"Наші досвідчені спеціалісти працюють над вашими проектами, забезпечуючи професійний підхід і високу якість виконання робіт.",
		img: personIcon,
		imgSize: [156, 189],
	},
	{
		id: 4,
		title: "Професійний супровід",
		descr:
			"Надаємо постійну підтримку та консультації на всіх етапах проекту, допомагаючи вам досягти поставлених цілей.",
		img: supportIcon,
		imgSize: [183, 189],
	},
]
</script>

<style lang="scss" scoped>
.why {
	height: 100vh;
	position: relative;

	&::before {
		content: "";
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-image: url("../../assets/images/wave-whyUs.svg");
		background-position: bottom;
		background-repeat: no-repeat;
		background-size: cover;
		background-color: rbga(#180b1c, 0.04);
		mix-blend-mode: luminosity;
		z-index: 1;
	}

	&__container {
		max-width: 1270px;
		margin: 84px auto 0;
		z-index: 3;
		position: relative;
	}

	&__top {
		position: relative;
		display: flex;
		z-index: 3;
		justify-content: space-between;
	}

	&__text {
		max-width: 672px;
		padding-top: 20px;
	}

	&__title {
		font-weight: 700;
		font-size: 55px;
		line-height: 110.6%;
		background: linear-gradient(91.2deg, #b5feef 10.31%, #2eecc5 165.09%);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		background-clip: text;
		text-fill-color: transparent;
		text-shadow: 0px 0px 36px rgba(165, 252, 235, 0.2);
	}

	&__descr {
		font-weight: 500;
		font-size: 17px;
		line-height: 21px;
		color: rgba(255, 255, 255, 0.65);
		margin-top: 18px;
		max-width: 670px;

		& span {
			margin-top: 41px;
			display: block;
		}
	}

	&__button {
		margin-top: 43px;
	}

	&__bottom {
		margin-top: 32px;
		display: flex;
		align-items: center;
		gap: 35px;
	}
}
</style>

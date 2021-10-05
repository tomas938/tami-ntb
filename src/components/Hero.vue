<template>
	<div class="hero">
		<img src="../assets/Hero/idk.png" alt="hero" />
		<div class="hero__content">
			<h1>Mliečna <br />chuť Tatier</h1>
			<span>v novom dizajne</span>
		</div>
		<div class="pagination">
			<span
				@click="goToSlide(index)"
				v-for="(slide, index) in slides"
				:key="index"
				:class="{ active: index + 1 === currentSlide }"
			></span>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			currentSlide: 1,
			slides: ["a", "b", "b", "d"],
		};
	},
	methods: {
		goToSlide(index) {
			this.currentSlide = index + 1;
		},
	},
};
</script>

<style lang="scss" scoped>
.hero {
	position: relative;

	&__content {
		position: absolute;
		top: 45%;
		left: 15%;
		transform: translateY(-50%);
	}
	h1 {
		font-size: 17rem;
		font-family: var(--hero-heading);
		color: white;
		text-shadow: 4px 4px 2px rgba(150, 150, 150, 1);
		@media only screen and (max-width: 1500px) {
			font-size: 10rem;
		}
		@media only screen and (max-width: 800px) {
			font-size: 7rem;
		}
		@media only screen and (max-width: 600px) {
			font-size: 5rem;
		}
		@media only screen and (max-width: 400px) {
			font-size: 4rem;
		}
	}
	span {
		color: var(--dark-blue);
		font-weight: bold;
		font-size: 4.8rem;
		@media only screen and (max-width: 800px) {
			font-size: 2.8rem;
		}
		@media only screen and (max-width: 600px) {
			font-size: 1.8rem;
		}
		@media only screen and (max-width: 400px) {
			font-size: 1.3rem;
		}
	}
	img {
		width: 100%;
	}
	.pagination {
		position: absolute;
		bottom: 7rem;
		@media only screen and (max-width: 1000px) {
			bottom: 4rem;
		}
		width: 100%;
		left: 50%;
		transform: translateX(-50%);
		display: flex;
		gap: 1.6rem;
		justify-content: center;
		align-items: center;
		span {
			cursor: pointer;
			width: 0.9rem;
			height: 0.9rem;
			border-radius: 50%;
			background-color: transparent;
			border: 2px solid var(--dark-blue);
		}
		.active {
			background-color: var(--dark-blue);
			transform: scale(0.7);
			&::before {
				content: "";
				position: absolute;
				top: -15px;
				right: -15px;
				bottom: -15px;
				left: -15px;
				border-radius: 50%;
				border: 4px solid #cfd8ea;
			}
		}
	}
}
</style>

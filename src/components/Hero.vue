<template>
	<div class="hero">
		<img src="../assets/Hero/idk.png" alt="hero" />
		<div class="hero__content">
			<h1>Mliečna <br />chuť Tatier</h1>
			<span>v novom dizajne</span>
		</div>
	</div>
</template>

<script>
export default {};
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
}
</style>

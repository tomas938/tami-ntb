<template>
	<router-link to="/" class="card">
		<img :src="require(`../assets/News/${img}.png`)" alt="news" />
		<div class="card__content">
			<h3>{{ heading }}</h3>
			<p>
				{{ description }}
			</p>
			<router-link to="/">čítať viac</router-link>
		</div>
	</router-link>
</template>

<script>
export default {
	props: ["heading", "description", "img"],
};
</script>

<style lang="scss" scoped>
.card {
	display: flex;
	flex-direction: column;
	background-color: white;
	max-width: 50rem;
	img {
		width: 100%;
		object-fit: cover;
	}
	&__content {
		padding: 4rem;
		h3 {
			font-size: 1.8rem;
			color: var(--dark-blue);
			margin-bottom: 2rem;
		}
		p {
			color: var(--news-p-color);
			margin-bottom: 4rem;
		}
		a {
			color: var(--danger);
		}
		h3,
		a {
			font-weight: bold;
			text-transform: uppercase;
		}
		p,
		a {
			font-size: 1.6rem;
		}
	}
}
</style>

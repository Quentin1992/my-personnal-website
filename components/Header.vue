<template>
	<header class="header">
		<nav>
			<ul>
				<li>
					<a href="#hero" @click.prevent="scrollToSection('hero')"
						>Accueil</a
					>
				</li>
				<li>
					<a href="#about" @click.prevent="scrollToSection('about')"
						>À propos</a
					>
				</li>
				<li>
					<a
						href="#projects"
						@click.prevent="scrollToSection('projects')"
						>Réalisations</a
					>
				</li>
				<li>
					<a
						href="#contact"
						@click.prevent="scrollToSection('contact')"
						>Contact</a
					>
				</li>
			</ul>
		</nav>
	</header>
</template>

<script>
export default {
	methods: {
		scrollToSection(id) {
			document.getElementById(id).scrollIntoView({ behavior: "smooth" });
		},
	},
};
</script>

<style scoped lang="scss">
.header {
	position: fixed;
	top: 0;
	width: 100%;
	background: var(--primaryColor);
	color: var(--lightColor);
	nav {
		ul {
			display: flex;
			list-style: none;
			justify-content: space-around;
			padding: 0;
			li a {
				color: var(--lightColor);
				text-decoration: none;
				padding: 1em;
			}
		}
	}
}
</style>

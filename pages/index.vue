<template>
	<div>
		<!-- Header avec navigation fixe -->
		<header class="header">
			<nav>
				<ul>
					<li><a href="#hero">Accueil</a></li>
					<li><a href="#about">À propos</a></li>
					<!-- <li><a href="#projects">Projets</a></li>
					<li><a href="#blog">Blog</a></li> -->
					<li><a href="#contact">Contact</a></li>
				</ul>
			</nav>
		</header>

		<!-- Section Héros -->
		<section id="hero" class="hero">
			<h1>Quentin Bogaert</h1>
			<p>
				Découvrez mes compétences pour créer des solutions web
				optimisées et accessibles.
			</p>
			<!-- <button @click="scrollToSection('#projects')">
				Découvrir mes projets
			</button> -->
		</section>

		<!-- Section À propos -->
		<section id="about" class="about">
			<h2>À propos de moi</h2>
			<p>
				Je suis développeur fullstack spécialisé en front, passionné par
				l'optimisation des processus de développement et la création
				d'applications performantes. J'apporte une attention
				particulière à chaque projet, en me concentrant sur la
				robustesse et la fonctionnalité. Mes compétences incluent :
			</p>
			<ul>
				<li>
					Analyse des besoins et mise en œuvre de solutions adaptées
				</li>
				<li>
					Développement front-end en HTML, CSS/SCSS, JavaScript et
					Vue.js, avec une attention particulière portée à
					l'intégration et à la performance
				</li>
				<li>
					Introduction au développement back-end avec Node.js et bases
					de données PostgreSQL, en apprenant à assurer une
					communication fluide entre le client et le serveur
				</li>
				<li>
					Optimisation de l'accessibilité et du SEO, garantissant que
					les applications sont accessibles et bien référencées
				</li>
				<li>
					Gestion des versions de code via Git, que ce soit localement
					ou sur des plateformes comme GitHub et Bitbucket
				</li>
				<li>
					Tests automatisés avec Jest pour assurer la qualité du code
				</li>
				<li>
					Documentation et gestion de projet à l'aide de Notion,
					favorisant la collaboration au sein des équipes
				</li>
				<li>
					Un engagement constant envers la qualité du code, en mettant
					l'accent sur la maintenabilité et la lisibilité
				</li>
			</ul>
			<p>
				Mon parcours atypique, qui débute par des études en électronique
				et en cinéma, m'a permis de développer une perspective unique
				sur le développement web, alliant technique et innovation. J'ai
				commencé comme développeur front-end, et je suis en train
				d'élargir mes compétences vers le développement back-end.
			</p>
			<p>
				Passionné par l'apprentissage continu et les nouvelles
				technologies, je suis toujours à la recherche de nouveaux défis
				à relever.
			</p>
		</section>

		<!-- Section Projets -->
		<!-- <section id="projects" class="projects">
			<h2>Mes projets</h2>
			<div
				v-for="(project, index) in projects"
				:key="index"
				class="project"
			>
				<h3>{{ project.title }}</h3>
				<p>{{ project.description }}</p>
			</div>
		</section> -->

		<!-- Section Blog -->
		<!-- <section id="blog" class="blog">
			<h2>Derniers articles de blog</h2>
			<div
				v-for="(post, index) in blogPosts"
				:key="index"
				class="blog-post"
			>
				<h3>{{ post.title }}</h3>
				<p>{{ post.summary }}</p>
			</div>
		</section> -->

		<!-- Section Contact -->
		<section id="contact" class="contact">
			<h2>Contact</h2>
			<p>
				Envie de me contacter ? Retrouvez-moi sur
				<a href="https://www.linkedin.com/in/quentin-bogaert/">
					LinkedIn </a
				>,
				<a
					href="https://welovedevs.com/app/user/quentin-developpeur-web-frontend"
				>
					WeLoveDevs </a
				>, ou <a href="https://github.com/Quentin1992"> GitHub </a>.
			</p>
		</section>

		<!-- Footer -->
		<footer class="footer">
			<p>&copy; 2024 TechBuilder</p>
			<nav>
				<a href="#hero">Mentions légales</a> |
				<a href="#privacy">Politique de confidentialité</a>
			</nav>
		</footer>
	</div>
</template>

<script>
export default {
	data() {
		return {
			projects: [
				{
					title: "To-do list TypeScript",
					description:
						"Une application de to-do list construite en TypeScript.",
				},
				{
					title: "Site vitrine personnel",
					description:
						"Mon site personnel pour présenter mes projets et articles.",
				},
			],
			blogPosts: [
				{
					title: "Pourquoi j'ai décidé d'apprendre TypeScript",
					summary: "Un article sur mes motivations...",
				},
				{
					title: "Installer et configurer TypeScript",
					summary: "Un guide pour débutants en TypeScript.",
				},
			],
		};
	},
	methods: {
		scrollToSection(id) {
			document.querySelector(id).scrollIntoView({ behavior: "smooth" });
		},
	},
};
</script>

<style scoped lang="scss">
/* Styles de base */
body {
	margin: 0;
}

.header {
	position: fixed;
	top: 0;
	width: 100%;
	background: #333;
	color: #fff;
	nav ul {
		display: flex;
		list-style: none;
		justify-content: space-around;
		padding: 0;
		li a {
			color: #fff;
			text-decoration: none;
			padding: 1em;
		}
	}
}
.hero,
.about,
.projects,
.blog,
.contact {
	padding: 4rem 2rem;
	min-height: 100vh;
}
.hero {
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	background: #f4f4f4;
}
.footer {
	background: #333;
	color: #fff;
	text-align: center;
	padding: 1rem;
}
</style>

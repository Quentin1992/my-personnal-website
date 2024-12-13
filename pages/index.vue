<template>
	<NuxtLayout>
		<!-- Section Héros -->
		<section id="hero" class="hero">
			<img src="../static/images/portrait.png" />
			<div>
				<h1>Quentin Bogaert</h1>
				<h2>Développeur Full-Stack | Spécialiste Front-End (Vue.js)</h2>
				<p>
					Découvrez mes compétences pour créer des solutions web
					optimisées et accessibles.
				</p>
				<div class="hero__links">
					<button @click="scrollToSection('about')">
						A propos de moi
					</button>
					<button @click="scrollToSection('contact')">Contact</button>
				</div>
			</div>
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
		<section id="projects" class="projects">
			<h2>Mes réalisations</h2>
			<div class="project">
				<img src="../static/images/projects/chaudmiretteprod.png" />
				<div>
					<h3>Chaud Mirette Productions</h3>
					<p>
						Site vitrine conçu pour une société de production
						audiovisuelle, intégrant un backoffice complet pour la
						gestion autonome des contenus.
					</p>
					<p>Technologies : PHP, JQuery, HTML 5, CSS 3</p>
					<p>
						Fonctionnalités : responsive, accessible, avec
						backoffice
					</p>
					<a
						href="https://github.com/Quentin1992/cmprod"
						target="_blank"
						>Voir le projet sur GitHub</a
					>
				</div>
			</div>
			<div class="project">
				<img src="../static/images/projects/to-do-list.png" />
				<div>
					<h3>To-do list (en cours)</h3>
					<p>
						Projet de to-do list développée dans le cadre de mon
						apprentissage de TypeScript. Il met en pratique des
						concepts fondamentaux tout en explorant les bonnes
						pratiques du développement.
					</p>
					<p>Technologies : Typescript, Vite, HTML 5, CSS 3</p>
					<p>
						Fonctionnalités : ajout, modification de l'état et
						suppression des tâches.
					</p>
					<a
						href="https://github.com/Quentin1992/todo-list-ts"
						target="_blank"
						>Voir le projet sur GitHub</a
					>
				</div>
			</div>
		</section>

		<!-- Section Contact -->
		<section id="contact" class="contact">
			<h2>Contact</h2>
			<p>
				Envie de me contacter ? Retrouvez-moi sur LinkedIn, WeLoveDevs,
				ou GitHub :
			</p>
			<div class="contact__links">
				<a href="https://www.linkedin.com/in/quentin-bogaert/">
					<img src="../static/images/icons/linkedin-logo.png" />
				</a>
				<a
					href="https://welovedevs.com/app/user/quentin-developpeur-web-frontend"
				>
					<img src="../static/images/icons/welovedevs-logo.svg"
				/></a>
				<a href="https://github.com/Quentin1992">
					<img src="../static/images/icons/github-logo.png"
				/></a>
			</div>
		</section>
	</NuxtLayout>
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
/* Styles de base */
.hero,
.about,
.projects,
.contact {
	padding: 4rem 2rem;
}
.about,
.projects,
.contact {
	@media (min-width: 900px) {
		width: 50%;
		margin: auto;
	}
}
.hero {
	min-height: 100vh;
}
.hero {
	display: flex;
	justify-content: center;
	align-items: center;
	gap: 1em;
	background-color: var(--lightColor);
	flex-direction: column;
	@media (min-width: 900px) {
		flex-direction: row;
	}
	h1 {
		font-size: 1.8em;
	}
	p {
		font-size: 1.3em;
	}
	img {
		width: 100px;
		height: 100px;
		border-radius: 50%;
		@media (min-width: 900px) {
			width: 200px;
			height: 200px;
		}
	}
	&__links {
		display: flex;
		gap: 1em;
	}
}
.projects {
	.project {
		margin-bottom: 3rem;
		@media (min-width: 900px) {
			display: flex;
			gap: 3em;
		}
		img {
			max-height: 180px;
			max-width: 100%;
			border: solid 2px var(--darkColor);
		}
	}
}
.contact {
	flex-direction: column;
	&__links {
		display: flex;
		justify-content: space-around;
		img {
			width: 50px;
			height: 50px;
			@media (min-width: 900px) {
				width: 100px;
				height: 100px;
			}
		}
	}
}
</style>

<template>
	<footer class="footer">
		<div class="legal-notice">
			<div>
				<h2>Éditeur du site</h2>
				<p>
					Quentin Bogaert<br />
					Contact :
					<a href="mailto:contact@quentinbogaert.com"
						>contact@quentinbogaert.com</a
					>
				</p>
			</div>
			<div>
				<h2>Hébergeur</h2>
				<p>
					Hostinger International Ltd.<br />
					Adresse : 61 Lordou Vironos Street, Larnaca, 6023, Chypre<br />
					Site web :
					<a href="https://www.hostinger.fr"
						>https://www.hostinger.fr</a
					>
				</p>
			</div>
		</div>

		<div class="credits">
			<p>&copy; 2024 Quentin Bogaert</p>
			<a
				href="https://www.flaticon.com/free-icons/linkedin"
				title="linkedin icons"
				>Linkedin icons created by Google</a
			>
			<a href="https://www.flaticon.com/free-icons/cat" title="cat icons"
				>Cat icons created by Dave Gandy</a
			>
		</div>
	</footer>
</template>

<style scoped lang="scss">
.footer {
	background: var(--darkColor);
	color: var(--lightColor);
	padding: 1rem;
	display: flex;
	justify-content: space-between;
	h2 {
		font-size: 1em;
	}
	p,
	a {
		font-size: 0.8rem;
	}
	a {
		color: var(--lightColor);
		&:visited {
			color: var(--primaryColor);
		}
	}
	.legal-notice {
		display: flex;
		gap: 1em;
	}
	.credits {
		display: flex;
		flex-direction: column;
	}
}
</style>

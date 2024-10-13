<template>
  <section class="homepage">
    <header>
      <h1>Bienvenue sur mon CV en ligne</h1>
      <p>Développeur web passionné, je vous invite à découvrir mes projets et mon parcours.</p>
    </header>

    <div class="intro">
      <h2>À propos de moi</h2>
      <p>
        Je suis un développeur spécialisé dans les technologies web comme JavaScript, TypeScript, et Vue.js.
        En constante évolution, je cherche à améliorer mes compétences et partager mon apprentissage.
      </p>
    </div>

    <div class="projects">
      <h2>Mes projets</h2>
      <ul>
        <li><a href="#">Projet 1</a></li>
        <li><a href="#">Projet 2</a></li>
      </ul>
    </div>
  </section>
</template>

<script lang="ts">
export default {
  name: 'HomePage',
}
</script>

<style scoped lang="scss">
.homepage {
  text-align: center;
  margin: 2rem;

  header {
    margin-bottom: 2rem;

    h1 {
      font-size: 2.5rem;
    }

    p {
      font-size: 1.2rem;
      color: #666;
    }
  }

  .intro {
    margin: 1.5rem 0;

    h2 {
      font-size: 2rem;
      margin-bottom: 1rem;
    }

    p {
      font-size: 1.1rem;
      color: #333;
    }
  }

  .projects {
    margin: 1.5rem 0;

    ul {
      list-style-type: none;
      padding: 0;

      li {
        margin: 0.5rem 0;

        a {
          color: #3498db;
          text-decoration: none;

          &:hover {
            text-decoration: underline;
          }
        }
      }
    }
  }
}
</style>
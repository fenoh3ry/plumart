<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="A propos de nous"
      subtitle=""
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>Qui nous sommes</h3>
          <p>
          Les membres sont tous des jeunes qui veulent évoluer dans le domaine de l'Art et ont  tous des styles de dessin différents: portrait, peinture, manga, BD, illustration ( tradi ou digi).......
          L'association a été fondée en 2014 (association a but non lucratif) et compte plus d'une cinquantaine de membres a ce jour . Nous siégeons actuellement au Global Hub Network Antsahavola.
          Le slogan de l'association est <b> " Évoquons l'artiste qu'on est " </b>
          Parmi nos objectifs, nous voulons promouvoir les jeunes artistes malagasy. Je veux parler là des jeunes qui n'en fait pas un travail mais un divertissement . Cette promotion se présente sous forme d'exposition, d'atelier de dessin, atelier de rencontre, échange et partage  ...
          </p>
        </div>
      </template>

      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Dernière publication 
        </h3>
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `A Propos | ${this.$siteConfig.siteName}`
    }
  },
  components: { QuoteCard }
}
</script>

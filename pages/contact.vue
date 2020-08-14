<template>
  <div id="contact-page" class="page-wrapper contact-page content-page">
    <site-hero
      title="Nous Contacter"
      subtitle=""
      image="/uploads/contact-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Salut!
              </p>
              <p class="subtitle">
                Tout d'abord laisser nous vous présenter Plum'Art.
              </p>
              <figure class="image is-1by1 ">
                <opti-image
                  :src="require('~/assets/uploads/contact-person.jpg').src"
                  :srcset="
                    require('~/assets/uploads/contact-person.jpg').srcSet
                  "
                />
              </figure>
              <br />
              <div class="content">
                <p>
                  <strong>
                   Plum'Art est une association de jeunes artistes Malagasy(15~27ans).
                  </strong>
                </p>
                <p>
                  Les membres sont tous des jeunes qui veulent évoluer dans le domaine de l'Art et ont  tous des styles de dessin différents: portrait, peinture, manga, BD, illustration ( tradi ou digi).......
L'association a été fondée en 2014 (association a but non lucratif) et compte plus d'une cinquantaine de membres a ce jour . Nous siégeons actuellement au Global Hub Network Antsahavola.
Le slogan de l'association est " Évoquons l'artiste qu'on est " 
Parmi nos objectifs, nous voulons promouvoir les jeunes artistes malagasy. Je veux parler là des jeunes qui n'en fait pas un travail mais un divertissement . Cette promotion se présente sous forme d'exposition, d'atelier de dessin, atelier de rencontre, échange et partage  ...
                </p>
              </div>
            </article>
          </div>
          <div class="tile is-parent is-8">
            <article class="tile is-child box">
              <contact-form />
            </article>
          </div>
        </div>
      </template>
      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <!-- Latest Posts -->
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import ContactForm from '~/components/ContactForm'
export default {
  head() {
    return {
      title: `Contact | ${this.$siteConfig.siteName}`
    }
  },
  components: { ContactForm }
}
</script>

<template lang="html">
  <div>
    <section>
      <v-parallax src="steph.jpg" height="600">
        <v-layout
          column
          justify-center
          class="white--text">
          <v-flex xs12 class="my-3">
            <div class="text-xs-center">
              <h2 class="mb-2">Stephane Villette</h2>
              <span class="intro white--text">Coloriste sur cuir</br></span>
            </div>
          </v-flex>
        </v-layout>
      </v-parallax>
    </section>

    <section>
      <v-layout
        column
        wrap
        align-center>
        <v-flex xs12 sm4 class="my-3">
          <div class="text-xs-center">
            <h3 class="headline"></h3>
          </div>
        </v-flex>

        <v-flex xs12>
          <v-container grid-list-xl>
            <v-layout row wrap justify-center>

              <v-flex xs12 md3>
                <v-card class="elevation-0 transparent">
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline">Portrait</div>
                  </v-card-title>
                  <v-card-text>
                    Stéphane a commencé à 21 ans sa carrière chez Hermès et se consacre très vite à l'entretien et la finition des chaussures sur mesure John Lobb. Entre 2006 et 2015 il offre ses services à la maison Corthay pour la finition des chaussures de luxe. Après 20 ans d'expérience dans ces prestigieuses enseignes, il est aujourd'hui un des rares spécialistes de l'art de la patine.

                  </v-card-text>
                </v-card>
              </v-flex>

              <v-flex xs12 md3>
                <v-card class="elevation-0 transparent">
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline text-xs-center">L'art de la patine</div>
                  </v-card-title>
                  <v-card-text>
                    La patine, c’est l'ensemble des techniques de coloration et décoloration du cuir, par l'application de solvants, huiles essentielles, pigments et teintures.
                    Comme pour une œuvre d’art, Stephane jongle avec les pigments, joue avec les teintures et les huiles essentielles. Il se sert, pour appliquer ses produits, de multitudes d’outils : pinceaux de toutes tailles, éponges, chiffons…
                </v-card-text>
              </v-card>
              </v-flex>

              <v-flex xs12 md3>
                <v-card class="elevation-0 transparent">
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline text-xs-center">Pourquoi faire patiner ses souliers ?</div>
                  </v-card-title>
                  <v-card-text>
                    La patine permet de rendre vos souliers uniques, faisant ressortir votre personnalité.
                </v-card-text>
              </v-card>
              </v-flex>
            </v-layout>
          </v-container>
        </v-flex>
      </v-layout>
    </section>
  <section class="partners-section">
    <v-container grid-list-x5 text-xs-center>
      <v-layout column wrap justify-center>
        <v-flex xs12  class="my-3">
          <div class="text-xs-center">
            <h3 class="headline"></h3>
          </div>
        </v-flex>

          <v-flex xs12>
            <v-container grid-list-x5>
              <v-layout row wrap justify-center>
                <v-flex xs12 md2 v-for="(partner, idx) in partners">
                  <h4 class="headline text-xs-center">{{ partner.brand }}</h4>
                </v-card-media>
                </v-flex>
              </v-layout>
            </v-container>
          </v-flex>
    </v-layout>
  </v-container>
  </section>


</div>
</template>

<script>
export default {
  name: 'section1',
  data: () => ({
    intro: '',
    partners: [
      {
        media: 'sjimenez.jpeg',
        brand: 'Stephane Jimenez'
        // link: ''
      },
      {
        media: 'jmalinge.png',
        brand: 'Joseph Malinge'
        // link:
      },
      {
        media: 'lcadet.png',
        brand: 'Lavabre Cadet'
        // link:
      },
      {
        media: 'lobb.png',
        brand: 'John Lobb'

        // link:
      },
      {
        media: 'corthay.png',
        brand: 'Corthay'
        // link:
      },
      {
        media: 'corthay.png',
        brand: 'Berluti'
        // link:
      }
    ],
    skills:
    [
      {
        name: 'HTML'
      },
      {
        name: 'CSS'
      },
      {
        name: 'Javascript'
      },
      {
        name: 'PHP'
      },
      {
        name: 'Responsive Design'
      },
      {
        name: 'Versioning'
      },
      {
        name: 'DevTools'
      },
      {
        name: 'Command Line'
      }
    ],
    languages: ['HTML', 'CSS', 'PHP', 'SQL'],
    frameworks: ['Vuejs', 'Bootstrap', 'Vuetify', 'Quasar', 'Element', 'Laravel'],
    BDD: ['PostgreSQL', 'MySQL'],
    librairies: ['Webpack', 'Lodash', 'Babel'],
    Versionnings: ['Git', 'Bitbucket']

  })
}
</script>

<style lang="css">
.card-picture{
  cursor: pointer;
  width: 100%;
}
.partners-section {
  padding-bottom: 10px;
}
.partners {
  width: auto;
  max-height: 10vh;
}
.partners-img {
  width: auto;
  height: auto;
}
.intro {
  font-family: monteCristo;
  font-size: 100px;
}
.subtitle{
  color: grey;
}
em{
  color: black;
  font-family: monteCristo;
}
.profile{
  width: auto;
  height: 150px;
  border-radius: 100px;
  border: solid;
  border-width: thick;
  border-color: grey;
}
.intro {
  color: #32353b;
  width: 50%;
}
.parallax__image{
  margin-bottom: 200px;
}
.parallax__content{
  margin-top: 145px;
justify-content: baseline;
}
.match{
  margin-top: 10px;
  width: 22%;
  display: flex;
  justify-content: space-between;
}
.my-5 {
    margin-top: 0;
    margin-bottom: 0;
}
</style>

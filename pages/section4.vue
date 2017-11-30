<template lang="html">
  <div>
    <section>
      <v-parallax src="sec4.jpg" height="600">
        <v-layout column align-center justify-center>
          <h2 class="mb-2 ">Réalisations</h2>

        </v-layout>
      </v-parallax>
    </section>

    <section>
      <v-layout
        column
        wrap
        class="my-5"
        align-center
      >
        <v-flex xs12 sm4 class="my-3">
          <div class="text-xs-center">
            <h3 class="headline">Cliquez sur les vignettes</h3>
            <span class="subheading">
              pour plus de détails
            </span>
          </div>
        </v-flex>
        <v-flex xs12>
          <v-container grid-list-xl>
            <v-layout row wrap align-center>
              <v-flex v-for="card in cards" xs12 md4>
                <v-card
                @mouseleave="card.show = false">
                  <v-card-media
                  @click.native="card.show = !card.show"
                    class="card-picture white--text"
                    height="200px"
                    :src="'../' + card.media">
                  <v-container fill-height fluid>
                    <v-layout fill-height>
                      <v-flex xs12 align-end flexbox>
                        <span class="card-title">{{ card.headline }}</span>
                      </v-flex>
                    </v-layout>
                  </v-container>
                </v-card-media>
                <v-card-text v-show="card.show">
                  {{ card.resume }}
                </v-card-text>
              </v-card>
              </v-flex>
            </v-layout>
          </v-container>
        </v-flex>
      </v-layout>
    </section>
</div>
</template>

<script>
export default {
  name: 'section4',
  data: () => ({
    cards: [
      {
        media: 'patine1.jpg',
        headline: 'Bespoke Shoe, Stéphane JIMENEZ',
        resume: '1 mois de bénévolat en avril 2015 pour l\'ONG Off grid aid afin de construire des abris écologiques résistant aux typhons. J\'ai pu découvrir la technologie "EarthBag", utilisant le sol sous nos pieds, des sacs et des barbelés.',
        type: 'Bénévolat',
        comp: 'Vuejs',
        show: false
      },
      {
        media: 'patine2.jpg',
        headline: 'Bespoke Shoe, Stéphane JIMENEZ',
        resume: 'Pendant 6 mois, de septembre 2014 à mars 2015, je suis parti à la découverte de la vie à Mexico grâce à mes amis Aubin et Romain pendant près de 3 mois. J\'ai ensuite pris mon sac à dos pour découvrir le reste du pays : grottes de Tolantongo, Puerto Escondido sur la côte ouest, les incroyables pyramides de Teotihuacan, Palenque, Chitzen Itza, la côte Est et la lagune de Bacalar, Playa del Carmen, Tulum…',
        type: 'CDI',
        comp: 'Business Plan',
        show: false
      },
      {
        media: 'patine3.jpg',
        headline: 'Bespoke Shoe, Stéphane JIMENEZ',
        resume: 'Juste après avoir quitté la Macif, je suis parti tout le mois de janvier 2014 afin de prêter mains fortes en tant que bénévole à l\'association A.S.V.O. Je suis resté une semaine avec les rangers du parc Manuel Antonio puis je suis parti dans la péninsule de Nicoya afin d\'aider à la sauvergarde des tortues. ',
        type: 'CDI',
        comp: 'Management',
        show: false
      },
      {
        company: 'MACIF',
        media: 'patine4.jpg',
        headline: 'Bespoke Shoe, Stéphane JIMENEZ',
        resume: 'Après 1 an passé dans le froid de la Mongolie, j\'ai rejoint mes amis Sebastien et Julien à Brisbane, sur la côte Est de l\' Australie. Après 3 mois passés dans cette ville, me voilà parti pour un road trip qui m\'amena à longer toute la côte : des Whitesundays à Cairns, de Cairns à Melbourne, de Melbourne à la Tasmanie, de la Tasmanie à Sydney.',
        type: 'CDI',
        comp: 'Management',
        show: false
      },
      {
        media: 'patine5.jpg',
        headline: 'Bespoke Shoe, Stéphane JIMENEZ',
        resume: 'En 2007, tout juste diplômé, j\'ai eu une énorme envie de changement et j\'ai tout naturellement postulé à une annonce un peu spéciale, celle du Ministère des Affaires étrangères qui cherchait un comptable pour l\'Ambassade de France dans un pays que je ne connaissais pas, mais dont la capitale m\'était oralement sympathique : Oulan-Bator. Je suis donc resté un an, le temps de mon Volontariat International. J\'en ai profité pour visiter ce somptueux pays, ses paysages infinis dénoués de câbles électriques, de routes, de tout...Un court road-trip m\'a amené à découvrir les steppes mongoles à cheval et le désert de Gobi à chameau. Cette expérience d\'un an m\'a, sans aucun doute, changé à jamais.',
        type: 'Volontariat International en Administration',
        comp: 'Management',
        show: false
      },
      {
        media: 'patine6.jpg',
        headline: 'Bespoke Shoe, Stéphane JIMENEZ',
        resume: 'En 2007, tout juste diplômé, j\'ai eu une énorme envie de changement et j\'ai tout naturellement postulé à une annonce un peu spéciale, celle du Ministère des Affaires étrangères qui cherchait un comptable pour l\'Ambassade de France dans un pays que je ne connaissais pas, mais dont la capitale m\'était oralement sympathique : Oulan-Bator. Je suis donc resté un an, le temps de mon Volontariat International. J\'en ai profité pour visiter ce somptueux pays, ses paysages infinis dénoués de câbles électriques, de routes, de tout...Un court road-trip m\'a amené à découvrir les steppes mongoles à cheval et le désert de Gobi à chameau. Cette expérience d\'un an m\'a, sans aucun doute, changé à jamais.',
        type: 'Volontariat International en Administration',
        comp: 'Management',
        show: false
      }
    ]
  })
}
</script>

<style lang="css">

.subheading {
  color: #270830;
}
.card-picture{
  cursor: pointer;
}
.card-title{
  text-align: center;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.44);
}
</style>

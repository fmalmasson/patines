<template lang="html">
  <div>
    <section>
      <v-parallax src="pinceaux.jpg" height="600">
        <v-layout column align-center justify-center>
          <h2 class="mb-2 ">Avant - Après</h2>

        </v-layout>
      </v-parallax>
    </section>

    <section>
      <v-container grid-list-xl>
        <v-layout row wrap justify-space-between align-center>
<!--
          <v-flex xs12>
            <v-container grid-list-xl>
              <v-layout row wrap align-center>
                <v-flex class="comparison" xs12 md4> -->

                  <div class="image-slider">
                    <div>
                      <img src="apres.jpg" />
                    </div>
                      <img src="avant.jpg" />
                  </div>



                <!-- </v-flex> -->
                <!-- <v-flex class="comparison" xs12 md4> -->

                  <div class="image-slider">
                    <div>
                      <img src="pat2a.jpg" />
                    </div>
                      <img src="pat2.jpg" />
                  </div>



                <!-- </v-flex> -->
                <!-- <v-flex class="comparison" xs12 md4> -->

                  <div class="image-slider">
                    <div>
                      <img src="pat3a.jpg" />
                    </div>
                      <img src="pat3.jpg" />
                  </div>



                <!-- </v-flex> -->
              <!-- </v-layout>
            </v-container>
          </v-flex> -->
        </v-layout>
      </v-container>
    </section>
</div>
</template>

<script>

export default {

  name: 'section2',
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
        headline: 'Mexique, Voyage',
        resume: 'Pendant 6 mois, de septembre 2014 à mars 2015, je suis parti à la découverte de la vie à Mexico grâce à mes amis Aubin et Romain pendant près de 3 mois. J\'ai ensuite pris mon sac à dos pour découvrir le reste du pays : grottes de Tolantongo, Puerto Escondido sur la côte ouest, les incroyables pyramides de Teotihuacan, Palenque, Chitzen Itza, la côte Est et la lagune de Bacalar, Playa del Carmen, Tulum…',
        type: 'CDI',
        comp: 'Business Plan',
        show: false
      },
      {
        media: 'patine3.jpg',
        headline: 'Costa-Rica, Bénévolat',
        resume: 'Juste après avoir quitté la Macif, je suis parti tout le mois de janvier 2014 afin de prêter mains fortes en tant que bénévole à l\'association A.S.V.O. Je suis resté une semaine avec les rangers du parc Manuel Antonio puis je suis parti dans la péninsule de Nicoya afin d\'aider à la sauvergarde des tortues. ',
        type: 'CDI',
        comp: 'Management',
        show: false
      },
      {
        company: 'MACIF',
        media: 'patine4.jpg',
        headline: 'Australie, Voyage',
        resume: 'Après 1 an passé dans le froid de la Mongolie, j\'ai rejoint mes amis Sebastien et Julien à Brisbane, sur la côte Est de l\' Australie. Après 3 mois passés dans cette ville, me voilà parti pour un road trip qui m\'amena à longer toute la côte : des Whitesundays à Cairns, de Cairns à Melbourne, de Melbourne à la Tasmanie, de la Tasmanie à Sydney.',
        type: 'CDI',
        comp: 'Management',
        show: false
      },
      {
        media: 'patine5.jpg',
        headline: 'Mongolie, V.I.A',
        resume: 'En 2007, tout juste diplômé, j\'ai eu une énorme envie de changement et j\'ai tout naturellement postulé à une annonce un peu spéciale, celle du Ministère des Affaires étrangères qui cherchait un comptable pour l\'Ambassade de France dans un pays que je ne connaissais pas, mais dont la capitale m\'était oralement sympathique : Oulan-Bator. Je suis donc resté un an, le temps de mon Volontariat International. J\'en ai profité pour visiter ce somptueux pays, ses paysages infinis dénoués de câbles électriques, de routes, de tout...Un court road-trip m\'a amené à découvrir les steppes mongoles à cheval et le désert de Gobi à chameau. Cette expérience d\'un an m\'a, sans aucun doute, changé à jamais.',
        type: 'Volontariat International en Administration',
        comp: 'Management',
        show: false
      },
      {
        media: 'japan.jpg',
        headline: 'Japon, Voyage',
        resume: 'Il faisait encore - 40°C lorsque mes premières vacances à l\'Ambassade sont arrivées du coup je suis allé au Japon. Après tout, de la Mongolie, c\'est quand même un peu moins loin que de la France. Je suis parti 3 semaines visiter Tokyo et j\'ai absolument adoré. Au final, j\'y trouvais moins de différences qu\'en Mongolie(des voitures, pas de trous dans les routes, des escalators, un métro ...). C\'est à peu près tout concernant les ressemblances avec la France, car le Japon c\'est quand même  un autre monde.j\'ai eu la chance de pouvoir y manger les meilleurs sushis de ma vie et passer un extraordinaire séjour.',
        type: 'Volontariat International en Administration',
        comp: 'Management',
        show: false
      },
      {
        media: 'thai.jpg',
        headline: 'Thaïlande, Voyages',
        resume: 'Je suis allé 2 fois en Thaïlande tellement j\'adore ce pays. En tout, j\'y suis resté plus de 1 mois. J\'ai passé mon diplôme de plongée "PADI" à Koh Tao, je suis allé faire du scooter au nord, à Chiang Mai, de l\'escalade au sud à Tonzai, des soirées trop bruyantes à Bangkok…',
        comp: 'Management',
        show: false
      },
      {
        media: 'vietnam.jpg',
        headline: 'Vietnam, Voyages',
        resume: 'J\'ai découvert le Vietnam en prolongation d\'un séjour en Thaïlande. Avec des amis, nous avons découvert ce pays du sud au nord: Ho Chi Min, Nha Trang, Hanoi et la splendide baie d\'Halong (une des plus belles choses que j\'ai pu voir).',
        type: 'Volontariat International en Administration',
        comp: 'Management',
        show: false
      },
      {
        media: 'hk.jpg',
        headline: 'Hong-Kong, université',
        resume: 'Que dire de cette expérience démesurée ! C\'était la 1ere fois que je prenais l\'avion et j\'ai atterri directement dans une des villes les plus densément peuplées du monde.C\'était aussi la 1ere fois que j\'allais en Asie et en plus j\'y allais pour étudier à la Fac, le pied. Cette ville m\'a fasciné et j\'ai eu la chance de rencontrer des personnes formidables. Cette aventure reste à jamais gravée en moi.',
        type: 'Volontariat International en Administration',
        comp: 'Management',
        show: false
      },
      {
        media: 'london.jpg',
        headline: 'Angletterre, Stage',
        resume: 'Londres a été le décor de mon premier stage en École de commerce dans un bureau situé en plein Oxford Circus. J\'y suis resté 3 mois pour un stage de comptabilité. J\'ai adoré l\'ambiance qui règne dans cette ville.',
        type: 'Volontariat International en Administration',
        comp: 'Management',
        show: false
      }
    ]
  }),
  methods: {
    skillsList (job) {
      return job.skills.join(' - ')
    }
  }
}
</script>

<style lang="css">
.image-slider {
	position:relative;
	display: inline-block;
	line-height: 0;
}
.image-slider img {
	user-select: none;
	max-width: 400px;
}
.image-slider > div {
	position: absolute;
	top: 0; bottom: 0; left: 0;
	width: 50%;
	max-width: 100%;
	overflow: hidden;
	resize: horizontal;
}
.image-slider > div:before {
	content: '';
	display: block;
	width: 13px;
	height: 13px;
	overflow: hidden;
	position: absolute;
	resize: horizontal;
	right: 3px; bottom: 3px;
	background-clip: content-box;
	background: linear-gradient(-45deg, #270830 50%, transparent 0);
	-webkit-filter: drop-shadow(0 0 2px black);
	filter: drop-shadow(0 0 2px black);
}
.container.grid-list-xl>.layout>.flex {
  padding: 0;
}
h2{
  font-size: 200px;
}
.my-5 {
    margin-top: 0;
    margin-bottom: 0;
}
@import url(https://fonts.googleapis.com/css?family=Roboto:300);
html {
  background: #ddd;
  height: 100%;
  width: 100%;
  font-family: roboto;
  font-weight: 300;
}

h1 {
  text-align: center;
  color: #2FB4E1;
  font-size: 2rem;
  line-height: 2rem;
  margin: 0;
}
</style>

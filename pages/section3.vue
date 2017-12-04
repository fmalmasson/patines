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
        align-center>
        <v-flex xs12  class="select-shoes">
          <v-select
              v-bind:items="selectSorted"
              v-model="selection"
              label="filtrer par marque"
              autocomplete
              clearable
            ></v-select>
        </v-flex>


        <div class="shoes-container">
          <v-container grid-list-x5>
            <v-layout row wrap justify-center>
          <v-flex class="cards-show" v-for="(card, index) in cards" xs12 sm6 md4 v-if="card.brand === selection || selection === ''">
            <v-card @mouseleave="card.show = false">
              <v-card-media
                @click.native.stop="set_img_source(index), dialog = true"
                class="card-picture white--text"
                height="250px"
                :src="card.media">
                <v-container fill-height fluid>
                  <v-layout fill-height>
                    <v-flex xs12 align-end flexbox>
                      <span class="card-title">{{ card.headline }}</span>
                    </v-flex>
                  </v-layout>
                </v-container>
              </v-card-media>
              <v-card-text v-show="card.show">
                {{ card.brand }}
              </v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs12>
            <v-dialog v-model="dialog" width="auto">
              <div class="show_pic_div">
                <v-btn fab dark small color="primary" @click.native.stop="prev_pic()">
                  <v-icon dark>fa-chevron-left</v-icon>
                </v-btn>
                <img class="show_pic" :src="this.cards[img_source].media"/>
                <v-btn fab dark small color="primary" @click.native.stop="next_pic()">
                  <v-icon dark>fa-chevron-right</v-icon>
                </v-btn>
              </div>
            </v-dialog>
          </v-flex>
        </v-layout>
      </v-container>
    </div>
  </v-layout>
    </section>
  </div>
</template>

<script>

export default {
  name: 'section4',
  data: () => ({
    selection: '',
    img_source: 0,
    dialog: false,
    items: [
      'S. Jimenez',
      'Lavabre Cadet',
      'Loding',
      'Crockett & Jones',
      'Berluti',
      'Corthay',
      'Lobb',
      'J. Melinge'
    ],
    cards: [
      {
        media: 'patine1.jpg',
        headline: 'Bespoke Shoe, Stéphane JIMENEZ',
        brand: 'S. Jimenez',
        type: 'Bénévolat',
        comp: 'Vuejs',
        show: false
      },
      {
        media: 'patine2.jpg',
        headline: 'Bespoke Shoe, Stéphane JIMENEZ',
        brand: 'Crockett & Jones',
        type: 'CDI',
        comp: 'Business Plan',
        show: false
      },
      {
        media: 'patine3.jpg',
        headline: 'Bespoke Shoe, Stéphane JIMENEZ',
        brand: 'S. Jimenez',
        type: 'CDI',
        comp: 'Management',
        show: false
      },
      {
        company: 'MACIF',
        media: 'patine4.jpg',
        headline: 'Bespoke Shoe, Stéphane JIMENEZ',
        brand: 'J. Malinge',
        type: 'CDI',
        comp: 'Management',
        show: false
      },
      {
        media: 'patine5.jpg',
        headline: 'Bespoke Shoe, Stéphane JIMENEZ',
        brand: 'Berluti',
        type: 'Volontariat International en Administration',
        comp: 'Management',
        show: false
      },
      {
        media: 'patine6.jpg',
        headline: 'Bespoke Shoe, Stéphane JIMENEZ',
        brand: 'Loding',
        type: 'Volontariat International en Administration',
        comp: 'Management',
        show: false
      },
      {
        media: 'maxsizejpg.jpg',
        headline: 'Bespoke Shoe, Stéphane JIMENEZ',
        brand: 'Lobb',
        type: 'Volontariat International en Administration',
        comp: 'Management',
        show: false
      }
    ]
  }),
  computed: {
    selectSorted () {
      return this.items.sort()
    }
  },
  methods: {
    set_img_source (idx) {
      this.img_source = idx
    },
    prev_pic () {
      if (this.img_source > 0) {
        this.img_source -= 1
      }
    },
    next_pic () {
      if (this.img_source < this.cards.length - 1) {
        this.img_source += 1
      }
    }
  }
}
</script>

<style lang="css" >
.shoes-container{
  width: 100vw;
}
.select-shoes {
  width: 27vw;
}
.cards-show {
  margin-bottom: 5px;
}
.show_pic_div {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.show_pic {
  max-height: 80vh;
  width: auto;
}
.subheading {
  color: #270830;
}
.card-picture{
  cursor: pointer;
  width: 100%;
}
.card-title{
  text-align: center;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.44);
}
</style>

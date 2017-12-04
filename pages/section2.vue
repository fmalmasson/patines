<template lang="html">
  <div>
    <section>
      <v-parallax src="pinceaux.jpg" height="600">
        <v-flex xs12 class="my-3">
          <div class="text-xs-center">
          <h2 class="mb-2">Avant - Après</h2>
        </div>
      </v-flex>
      </v-parallax>
    </section>

    <section>
      <v-container grid-list-xl>
        <v-layout row wrap justify-space-between align-center>
          <v-flex v-for="(beforeAfter, idx) in beforeAfters" xs12 md4>
            <v-card class="elevation-0 transparent">
              <v-card-title primary-title class="layout justify-center">
                <div class="headline text-xs-center">{{ beforeAfter.title }}</div>
              </v-card-title>
              <div class="image-slider">
                <div>
                  <img :src="beforeAfter.apres" />
                </div>
                  <img :src="beforeAfter.avant" />
              </div>
          </v-card>
          </v-flex>


        </v-layout>
      </v-container>
    </section>

</div>
</template>

<script>

export default {

  name: 'section2',
  data: () => ({

    beforeAfters: [{
      'title': 'avant apres patine 1',
      'avant': 'avant.jpg',
      'apres': 'apres.jpg'
    },
    {
      'title': 'avant apres patine 2',
      'avant': 'pat2.jpg',
      'apres': 'pat2a.jpg'
    },
    {
      'title': 'avant apres patine 3',
      'avant': 'pat3.jpg',
      'apres': 'pat3a.jpg'
    },
    {
      'title': 'avant apres patine 1',
      'avant': 'avant.jpg',
      'apres': 'apres.jpg'
    },
    {
      'title': 'avant apres patine 2',
      'avant': 'pat2.jpg',
      'apres': 'pat2a.jpg'
    },
    {
      'title': 'avant apres patine 3',
      'avant': 'pat3.jpg',
      'apres': 'pat3a.jpg'
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
.card {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.image-slider {
	position:relative;
	display: inline-block;
	line-height: 0;
}
.image-slider img {
	user-select: none;
	max-height: 400px;
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

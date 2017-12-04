<template lang="html">
  <div id="app">
    <v-app light>
     <main>
       <section1 id="home"></section1>
       <section2 id="before-after"></section2>
       <!-- <section3 id="formation"></section3> -->
       <section3 id="production"></section3>

       <v-footer class="foot">
         <div class="white--text ml-3">
           Made with
           <v-icon class="red--text">favorite</v-icon>
           by Fabien Malmasson
         </div>
       </v-footer>
     </main>
   </v-app>
  </div>

</template>

<script>
import section1 from './section1.vue'
import section2 from './section2.vue'
import section3 from './section3.vue'

export default {
  components: {
    section1,
    section2,
    section3
  },
  data: () => ({
    title: 'Stephane Villette'
  })
}
</script>

<style lang="css">
.subtitle{
  color: #1697f6;
}
.foot{
  display: flex;
  justify-content: center;
  background-image: linear-gradient(to right, black, #270830);
}
#home, #before-after {
  background-color: black;
  /*height: 100vh;*/
}
#production {
  min-height: 100vh;
}
</style>

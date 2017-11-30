<template lang="html">
  <v-toolbar fixed>
    <div>
    <v-toolbar-title class="grey--text darken-2">Stephane Villette<span class="title-end"></span></v-toolbar-title>
    </div>
    <v-btn icon class="white--text"
      v-for="icon in icons"
      :href="icon.link"
      v-tooltip:bottom="{ html: icon.tooltip }"
      >
      <v-icon>{{ icon.name }}</v-icon>
    </v-btn>
    <v-spacer></v-spacer>

    <div class="item grey--text darken-2" v-for="(item, index) in items">
      <router-link :to="item.link">{{ item.title }}</router-link>
    </div>
    <router-link to="#home"><v-icon >home</v-icon></router-link>
  </v-toolbar>
</template>

<script>
export default {
  name: 'navbar',
  data: () => ({
    title: 'Fab',
    items: [{
      title: 'Avant / Après',
      link: '#experience-pro'
    },
    {
      title: 'Réalisations',
      link: '#international'
    }
    ],
    icons: [{
      name: 'fa fa-facebook-official',
      link: 'https://github.com/iiseej',
      tooltip: 'profil Facebook'
    },
    {
      name: 'fa-linkedin',
      link: 'https://linkedin.com/in/fabien-malmasson-564b881b',
      tooltip: 'profil Linkedin'
    },
    {
      name: 'fa-instagram',
      link: 'https://linkedin.com/in/fabien-malmasson-564b881b',
      tooltip: 'profil instagram'
    },
    {
      name: 'fa-youtube',
      link: 'https://linkedin.com/in/fabien-malmasson-564b881b',
      tooltip: 'profil Youtube'
    },
    {
      name: 'fa-google-plus-square',
      link: 'https://linkedin.com/in/fabien-malmasson-564b881b',
      tooltip: 'profil Google+'
    },
    {
      name: 'fa-envelope',
      link: 'mailto:stephanevillette49@gmail.com',
      tooltip: 'stephanevillette49@gmail.com'
    }
    ]
  })
}
</script>

<style scoped lang="css">

a{
  font-family: 'Roboto';
  font-weight: 400;
  font-style: normal;
  font-size: 13px;
  letter-spacing: .15em;
  text-transform: uppercase;
  color: rgb(110, 110, 110);
  text-decoration: none;
}
a:hover{
  color: black;
}
.item {
  font-weight: 700;
  font-style: normal;
  font-size: 13px;
  letter-spacing: .15em;
  text-transform: uppercase;
  margin: 10px;
  cursor: pointer;
}
.toolbar__content .item :hover   {
color: white;
}
/*.application--light .toolbar {
    background-color: transparent;
    color: rgba(0,0,0,.87);
}*/
.menu_block{
  position: fixed;
  z-index: 9999;
  left: 0;
  top: 0;
  right: 0;
  height: 80px;
  width: 100%;
  background-color: #fff;
  box-shadow: 0 2px 3px rgba(0,0,0,0.1)
}
.title-end{
font-weight: 700px;
color: black;
}
.toolbar__title {
  line-height: 80px;
    font-size: 20px;
    font-weight: 500;
    letter-spacing: .20em;
    margin-left: 16px;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
    /*color: grey;*/
    padding-right: 30px;
}
.profile{
  width: auto;
  height: 64px;
}
.menu-icon{
  margin-right: 5px;
}
</style>

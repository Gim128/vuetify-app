<template>
  <v-app>
     <Header />
    <v-main>

      <!-- hero section -->
      <hero-component />

      <!-- about us -->
      <AboutusComponent />
    </v-main>
  </v-app>
</template>

<script>

import Header from "./components/Header.vue";
import HeroComponent from '@/components/HeroComponent';
import AboutusComponent from "./components/AboutusComponent.vue";


export default {
  name: 'App',
  components: { HeroComponent, Header, AboutusComponent },
  data(){
    return {
      menus:[
        {title:'Home', route:'home'},
        {title:'About us', route:'about-us'},
        {title:'Portfolio', route:'portfolio'},
        {title:'Project', route:'project'},
        {title:'Gallery', route:'gallery'},
        {title:'Contact', route:'contact'}
      ]
    }
  }
};
</script>
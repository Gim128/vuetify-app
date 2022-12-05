<template>
  <v-app>
     <Header />
    <v-main>

      <!-- hero section -->
      <hero-component />

      <!-- about us -->
      <AboutusComponent />

      <!-- portfolio -->
      <PortfolioComponentVue />

      <!-- project -->
      <ProjectComponent />

      <!-- gallery -->
      <GalleryComponent />

      <!-- contactus -->
      <ContactFormComponentVue />

      <!-- footer -->
      <FooterComponent />

    </v-main>
  </v-app>
</template>

<script>

import Header from "./components/Header.vue";
import HeroComponent from '@/components/HeroComponent';
import AboutusComponent from "./components/AboutusComponent.vue";
import PortfolioComponentVue from "./components/PortfolioComponent.vue";
import ProjectComponent from "./components/ProjectComponent.vue";
import GalleryComponent from "./components/GalleryComponent.vue";
import ContactFormComponentVue from "./components/ContactFormComponent.vue";
import FooterComponent from "./components/FooterComponent.vue";


export default {
  name: 'App',
  components: { HeroComponent, Header, AboutusComponent, PortfolioComponentVue, ProjectComponent, GalleryComponent, ContactFormComponentVue, FooterComponent},
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
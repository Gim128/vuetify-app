<template>
   
    <v-app-bar

      style="padding:0px 90px"

      app
      color="white"
      light
      elevation="6"
      elevate-on-scroll
    >

    <v-toolbar-title>
      LeoLabs
    </v-toolbar-title>

    <v-spacer />

    <v-list class="d-flex align-center">
      <v-list-item link v-for="(menu,index) in menus" :key="index" :to="menu.route">
        <v-list-item-title> {{menu.title}} </v-list-item-title>
      </v-list-item>

      <v-btn text>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn outlined color="success">
        Get Start
      </v-btn>

    </v-list>
      
    </v-app-bar>
</template>

<script>
export default {
    
    // eslint-disable-next-line vue/multi-word-component-names
    name: "Header",
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
}
</script>

<style scoped>
.v-toolbar__title {
  font-family: Arial;
  font-weight: 700;
  color: #4caf50;
  font-size: 32px;
  line-height: 1.5;
}
</style>
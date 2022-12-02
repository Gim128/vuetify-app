<template>
  <v-app>
    <v-app-bar

      style="padding:0px 90px"

      app
      color="white"
      light
      elevation="6"
      elevate-on-scroll
    >

    <v-toolbar-title>
      Vuetify
    </v-toolbar-title>

    <v-spacer />

    <v-list>
      <v-list-item>
        <v-list-item-title> Home </v-list-item-title>
      </v-list-item>

      <v-list-item>
        <v-list-item-title> About </v-list-item-title>
      </v-list-item>

      <v-list-item>
        <v-list-item-title> Home </v-list-item-title>
      </v-list-item>

      <v-list-item>
        <v-list-item-title> Home </v-list-item-title>
      </v-list-item>

      <v-list-item>
        <v-list-item-title> Home </v-list-item-title>
      </v-list-item>

    </v-list>
      
    </v-app-bar>
      Vuetify
    <v-main>
      
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

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

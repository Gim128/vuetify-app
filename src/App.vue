<template>
  
  <v-app>
     
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

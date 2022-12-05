<template>
    <v-container class="pt-15">
        <v-row>
            <v-col lg="6">
                <h2 class="intro-text">Welcome to my vuetify app</h2>
                <p class="desc">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Natus aperiam eos, tempore modi porro optio recusandae quae necessitatibus repellendus expedita!</p>
                <v-btn color="success" class="white--text mr-10" rounded>Get Started</v-btn>
                <v-btn color="indigo" class="white--text" rounded>
                    <v-icon>mdi-play-circle</v-icon> Watch video
                </v-btn>
            </v-col>
                
            <v-col lg="6">
                <img width="100%" src="https://img.freepik.com/free-vector/happy-freelancer-with-computer-home-young-man-sitting-armchair-using-laptop-chatting-online-smiling-vector-illustration-distance-work-online-learning-freelance_74855-8401.jpg?w=1060&t=st=1670214908~exp=1670215508~hmac=01237830d29b77bebed88ae57536e393e906ffd7584496fc787657ca48c373e1" alt="hero-image">
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    h2.intro-text {
        font-size: 60px;
        font-weight: bold;
        font-family: Arial, Helvetica, sans-serif;
        color: #444;
    }

    p.desc{
        font-size: 19px;
        font-family: Arial, Helvetica, sans-serif;
        margin: 32px 0px;
        color: #444444ba;
    }

</style>
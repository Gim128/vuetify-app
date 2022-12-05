<template>
    <v-container my-15>
        <v-row justify="center">
            <v-col lg="12" class="text-center ">
                <v-subheader class="text-h4 justify-center">Portfolio</v-subheader>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod, porro.</p>
            </v-col>
           <v-col lg="12">
            <div class="text-center">
                <v-chip @click="activePortfolio = 'webapp'" :color="activePortfolio === 'webapp' ? 'success':''" class="mx-5">Web App</v-chip>
                <v-chip @click="activePortfolio = 'mobileapp'" :color="activePortfolio === 'mobileapp' ? 'success':''" class="mx-5">Mobile App</v-chip>
                <v-chip @click="activePortfolio = 'sketchdesign'" :color="activePortfolio === 'sketchdesign' ? 'success':''" class="mx-5">Sketch-Design </v-chip>
            </div>
           </v-col>

           <slot v-if="activePortfolio === 'webapp'">
                <v-col lg="3" v-for="(web,webindex) in webApps" :key="webindex">
                    <v-card>
                        <v-img
                        :src="web.image"
                        class="white--text align-end"
                        gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                        height="200px"
                        >
                        <v-card-title>{{web.title}}</v-card-title>
                        </v-img>
            
                        
                    </v-card>
                </v-col>
           </slot>

           <slot v-if="activePortfolio === 'mobileapp'">
            <v-col lg="3" v-for="(mobile,mobileindex) in mobileapp" :key="mobileindex">
                <v-card>
                    <v-img
                    :src=" mobile.image"
                    class="white--text align-end"
                    gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                    height="200px"
                    >
                    <v-card-title>{{mobile.title}}</v-card-title>
                    </v-img>
        
                    
                </v-card>
            </v-col>
       </slot>

       <slot v-if="activePortfolio === 'sketchdesign'">
            <v-col lg="3" v-for="(sketh,skethindex) in sketchdesign" :key="skethindex">
                <v-card>
                    <v-img
                    :src=" sketh.image"
                    class="white--text align-end"
                    gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                    height="200px"
                    >
                    <v-card-title>{{sketh.title}}</v-card-title>
                    </v-img>
        
                    
                </v-card>
            </v-col>
       </slot>
               
        </v-row>
    </v-container>
</template>

<script>
    export default {
        name: "PortfolioComponent",
        data(){
            return{
                activePortfolio:'webApp',
                webApps: [
                    {title:'web App 1',image:'https://img.freepik.com/free-vector/web-development-programmer-engineering-coding-website-augmented-reality-interface-screens-developer-project-engineer-programming-software-application-design-cartoon-illustration_107791-3863.jpg?w=1060&t=st=1670215656~exp=1670216256~hmac=33104f53f701644c92cc725a0f387e53c4d90c55534429ca1613b7be0cc7e7b9'},
                    {title:'web App 2',image:'https://img.freepik.com/premium-vector/web-ui-ux-design-web-development-concept-web-design-application-design-coding-web-building-white-background-3d-vector-illustration_145666-1590.jpg?w=1060'},
                    {title:'web App 3',image:'https://img.freepik.com/free-vector/tiny-developers-programming-website-internet-platform-flat-vector-illustration-cartoon-programmers-near-screen-with-open-code-script-software-development-digital-technology-concept_74855-10168.jpg?w=1060&t=st=1670215737~exp=1670216337~hmac=221f38b35890724cf544e31e5edad15b0a6e574c995d37360e99f1f17dc59b47'},
                    {title:'web App 4',image:'https://img.freepik.com/free-vector/seo-analytics-team-concept-illustration_114360-9205.jpg?w=1060&t=st=1670215762~exp=1670216362~hmac=b5a02a035eb2ee44bbf8fd28f3b319f77baaaa4a211228d59c981f64ab38a7d7'},
                    {title:'web App 5',image:'https://img.freepik.com/free-vector/digital-marketing-banner_157027-1372.jpg?w=1060&t=st=1670215888~exp=1670216488~hmac=0daf2efeff4ec4ff95eef2deb8414b7218a96999b841dfaa3ee409d8c905e703'},
                    {title:'web App 6',image:'https://img.freepik.com/free-vector/pair-programming-concept-illustration_114360-3941.jpg?w=1060&t=st=1670215928~exp=1670216528~hmac=859ebce15f1dcec9dcdc35f28c3d7f548487c4b040c2641747f5e5405f593433'},
                    {title:'web App 7',image:'https://img.freepik.com/free-vector/web-designers-ui-ux-have-consider-both-aesthetics-ease-use-that-will-confuse-users-vector-cartoon-illustration-flat-design_1150-56227.jpg?w=1060&t=st=1670216018~exp=1670216618~hmac=1bb929bb20d080dc5099a2615873650456588b1ba6038e7a425ceecc5f8f5ec3'},
                    {title:'web App 8',image:'https://img.freepik.com/free-vector/content-management-online-service-platform-idea-digital-strategy-content-social-network-website-promotion-online-post-control-system-vector-illustration_613284-3205.jpg?w=826&t=st=1670216120~exp=1670216720~hmac=013114620aa97bfed44431e98b7592a110e9dae529d7f5dee2274d90ddde92e8'},
                    
                ],
                mobileapp:[
                    {title:'mobile app 1',image:'https://img.freepik.com/free-vector/instagram-carousel-templates-with-photos_52683-52187.jpg?w=1060&t=st=1670216246~exp=1670216846~hmac=871c7c4d85f39dac9417abd7cfb3844f596edbc994bafd8254f6ced29ac01d21'},
                    {title:'mobile app 2',image:'https://img.freepik.com/free-vector/online-application-call-taxi-service-by-smart-phone_1150-48822.jpg?w=1060&t=st=1670216285~exp=1670216885~hmac=79203401b8891384eaf6b712159486b222313c8de5c1e9aaf347b47b8555f01d'},
                    {title:'mobile app 3',image:'https://img.freepik.com/free-vector/app-development-illustration_52683-47931.jpg?w=1060&t=st=1670216425~exp=1670217025~hmac=8239147cec4bf6218d0ead5517fe41dc637bd896e94faed6cbdb1ea9d96cc962'},
                    {title:'mobile app 4',image:'https://img.freepik.com/free-vector/smartphone-with-open-pages-landing-page_52683-22969.jpg?w=740&t=st=1670216493~exp=1670217093~hmac=5a024a3bf7799051499652dd64767c2fb950a62d5aa6d017420f5b555754b9e7'},
                    {title:'mobile app 5',image:'https://img.freepik.com/free-vector/game-development-concept-creative-process-computer-video-game-design-digital-technology-programming-codding-testing-isolated-flat-vector-illustration_613284-3265.jpg?w=740&t=st=1670216570~exp=1670217170~hmac=ef2bd08ba5f4ccdde957e54c5c5949773cc481e1d5b7bb444d1f86c00b4f0468'},
                    {title:'mobile app 6',image:'https://img.freepik.com/free-vector/application-programming-interface-concept-set-software-development-process-website-interface-design-improvement-programming-coding-it-profession-isolated-flat-vector-illustration_613284-2579.jpg?w=740&t=st=1670216616~exp=1670217216~hmac=5a1fc7fed9d7b1354df46d6f66200f812ba8f3eba2b4bab300eefafeca917af5'},
                ],
                sketchdesign:[
                    {title:'Sketh design 1',image:'https://img.freepik.com/free-vector/mobile-wireframe-concept-illustration_114360-5214.jpg?w=740&t=st=1670217547~exp=1670218147~hmac=10ab078e74cb17cc6447b88f83469ff3ee1689ab3d7a1470f684183ec6f9b1fb'},
                    {title:'Sketh design 2',image:'https://img.freepik.com/free-vector/flat-design-ui-ux-background_23-2149093994.jpg?w=1060&t=st=1670218235~exp=1670218835~hmac=2a1145564c92d2f27d02ba38c1f38ad3454f3554c2ca18afcff6545b9fffde0a'},
                    {title:'Sketh design 3',image:'https://img.freepik.com/free-vector/flat-design-ui-ux-background_23-2149093995.jpg?t=st=1670210346~exp=1670210946~hmac=8c56dae203e5ad2d56faa624e413b238cff95ea9ec35b8f62501c9dfe5032783'},
                    {title:'Sketh design 4',image:'https://img.freepik.com/free-vector/ui-ux-design-concept-illustration_114360-11214.jpg?w=1060&t=st=1670218300~exp=1670218900~hmac=33aaa96c106ee3ad88d06272243d8bd3ae28705c21a2f7d531ff0e0fe7846952'},
                    {title:'Sketh design 5',image:'https://img.freepik.com/free-vector/ux-ui-typographic-header-app-interface-improvement-user-interface-design-user-experience-development-modern-technology-concept-flat-vector-illustration_613284-1484.jpg?w=1380&t=st=1670218442~exp=1670219042~hmac=869ec8d67ce19e1d4b1a3acd6b3f33cf0958eee30732f8ceda7112b20fbfe8c4'},
                    {title:'Sketh design 6',image:'https://img.freepik.com/free-vector/web-design-concept-with-flat-style_23-2147854553.jpg?w=740&t=st=1670218531~exp=1670219131~hmac=a33c3fd18eedc02019cebdae873d08204c9742a87cb6be0fb316da896509c936'},
                ]
            }
        }
    }
</script>

<style scoped>
    

</style>
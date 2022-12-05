<template>
    <v-container my-15>
        <v-row justify="center">
            <v-col lg="12" class="text-center ">
                <v-subheader class="text-h4 justify-center">Contact Us</v-subheader>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod, porro.</p>
            </v-col>

            <v-col lg="5">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3960.774030926532!2d79.85067622240776!3d6.9175970044106005!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3ae2596b1c2ae5b1%3A0x872e9262f485d782!2sColombo%20City%20Centre%20Mall%20and%20Residences!5e0!3m2!1sen!2slk!4v1670228509628!5m2!1sen!2slk" width="450" height="100%" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
            </v-col>

            <v-col lg="7">
                <v-form ref="form">
                        <v-text-field
                        v-model="contactInfo.name"
                        :counter="10"
                        label="Name"
                      ></v-text-field>
                    
                        <v-text-field
                          v-model="contactInfo.email"
                          label="E-mail"
                          required
                        ></v-text-field>

                        <v-textarea label="Massage" v-model="contactInfo.masage">
                            
                        </v-textarea>

                        <v-btn
                        color="success"
                        class="mr-4"
                        >
                        Send
                        </v-btn>
                </v-form>
            </v-col>

        </v-row>
    </v-container>    
</template>

<script>
export default {
    name: "ContactFormComponent",
    data(){
        return{
            contactInfo:{}
        }
    }
}
</script>

<style scoped>

</style>
<template>
    <v-footer padless>

        <v-col lg="12">
            <v-row justify="center">
                <v-col lg="4" class="text-center">
                    <v-toolbar-title>LeoLabs</v-toolbar-title>
                    <v-card-text>
                        <v-btn
                          v-for="icon in icons"
                          :key="icon"
                          class="mx-4 black--text"
                          icon
                        >
                          <v-icon size="24px">
                            {{ icon }}
                          </v-icon>
                        </v-btn>
                      </v-card-text>
                      <v-subheader>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid quaerat quisquam, error asperiores velit placeat labore deserunt rem architecto tenetur?
                      </v-subheader>
                      <v-form class="mt-4">
                        <v-text-field label="Email" outlined dense />
                        <v-btn rounded color="success">Subscribe</v-btn>
                      </v-form>
                </v-col>
            </v-row>
            <div class="mt-10">
                <v-divider></v-divider>
                <v-subheader>
                    @ Copyright LeoLabs. All Rights Reserved! {{ new Date().getFullYear() }} — <strong>LeoLabs</strong>
                    <v-spacer />
                    <strong>Designed By Leo Munasinghe</strong>
                </v-subheader>
            </div>
        </v-col>


    <v-card
      flat
      tile
      class="indigo lighten-1 white--text text-center"
    >
      

      <v-card-text class="white--text pt-0">
        Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>DreamLabs</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
    name: "FooterComponent",
    data: () => ({
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    }),
}
</script>

<style>
    .v-toolbar__title {
        font-family: Arial;
        font-weight: 700;
        color: #4caf50;
        font-size: 32px;
        line-height: 1.5;
    }
</style>
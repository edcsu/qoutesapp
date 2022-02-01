<template>
  <v-app >
    <v-app-bar flat fixed app>
      <v-toolbar-title v-text="title" />
      <v-spacer />
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer
      app
      padless
    >
    <v-card
      flat
      tile
      class="text-center flex grey lighten-4"
    >
      <v-card-text>
        <v-tooltip color="purple lighten-2" top nudge-left="0">
          <template v-slot:activator="{ on }">
            <v-btn
              href="https://www.github.com/edcsu"
              target="_blank"
              icon
              class="mx-4"
              v-on="on"
            >
              <v-icon size="24px">mdi-github</v-icon>
            </v-btn>
          </template>
          <span>
            View
            <v-icon class="white--text">mdi-hand-pointing-down</v-icon>
          </span>
        </v-tooltip>
        <v-tooltip color="purple lighten-2" top nudge-left="0">
          <template v-slot:activator="{ on }">
            <v-btn
              href="https://www.linkedin.com/in/ssewannonda-keith-edwin-443303129"
              target="_blank"
              icon
              class="mx-4"
              v-on="on"
            >
              <v-icon size="24px">mdi-linkedin</v-icon>
            </v-btn>
          </template>
          <span>
            Connect
            <v-icon class="white--text">mdi-hand-pointing-down</v-icon>
          </span>
        </v-tooltip>
        <v-tooltip color="purple lighten-2" top nudge-left="0">
          <template v-slot:activator="{ on }">
            <v-btn
              href="https://twitter.com/skeith696"
              target="_blank"
              icon
              v-on="on"
              class="mx-4"
            >
              <v-icon size="24px">mdi-twitter</v-icon>
            </v-btn>
          </template>
          <span>
            Follow
            <v-icon class="white--text">mdi-hand-pointing-down</v-icon>
          </span>
        </v-tooltip>
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="">
        {{ new Date().getFullYear() }} — <strong>Made with 
          <v-icon class="mr-1 red--text">
            mdi-heart
          </v-icon> 
          &copy;Keith</strong>
      </v-card-text>
    </v-card>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      title: 'Random Quote App',
    }
  },
}
</script>

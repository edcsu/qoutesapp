<template>
  <v-app >
    <v-app-bar :clipped-left="clipped" fixed app>
      <v-toolbar-title v-text="title" />
      <v-spacer />
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
      <v-tooltip color="purple lighten-2" top nudge-left="70">
        <template v-slot:activator="{ on }">
          <v-btn
            href="https://www.linkedin.com/in/ssewannonda-keith-edwin-443303129"
            target="_blank"
            icon
            v-on="on"
          >
            <v-icon>mdi-linkedin</v-icon>
          </v-btn>
        </template>
        <span>
          Connect on LinkedIn
          <v-icon class="">mdi-hand-pointing-down</v-icon>
        </span>
      </v-tooltip>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Random Quote App',
    }
  },
}
</script>

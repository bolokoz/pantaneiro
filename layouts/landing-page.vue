<template>
  <v-app>
    <v-toolbar class="navbar py-5" color="transparent" flat absolute>
      <v-container class="d-flex">
        <div class="grey--text font-weight-light mb-2 text-h4">Flats |</div>
        <div class="font-weight-black text-h4">O Pantaneiro</div>
        <v-spacer />

        <v-toolbar-items class="d-none d-md-block">
          <v-btn v-scroll-reveal.reset="revealItem" text>Sobre</v-btn>
          <v-btn v-scroll-reveal.reset="revealItem" text>Wholesale</v-btn>
          <v-btn v-scroll-reveal.reset="revealItem" text>Locations</v-btn>
          <v-btn v-scroll-reveal.reset="revealItem" text>Our Story</v-btn>
        </v-toolbar-items>
        <v-btn v-scroll-reveal.reset="revealItem" icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>
        <v-btn v-scroll-reveal.reset="revealItem" icon>
          <v-icon>mdi-account-circle-outline</v-icon>
        </v-btn>
        <v-app-bar-nav-icon class="d-md-none"></v-app-bar-nav-icon>
      </v-container>
    </v-toolbar>

    <v-main> <nuxt /> </v-main>
    <v-fab-transition>
      <v-btn
        color="green lighten-1"
        fab
        fixed
        bottom
        right
        light
        class="v-btn--example"
        elevation="10"
      >
        <v-icon>mdi-whatsapp</v-icon>
      </v-btn>
    </v-fab-transition>
    <v-footer dark>
      <v-container class="d-flex grey--text text--darken-1 font-weight-medium">
        <span>Site feito por EngeBeck &copy; 2022</span> <v-spacer />
        <span>67 99976-78935</span>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      revealItem: {
        distance: '50%',
        origin: 'right',
      },
    }
  },
}
</script>

<style lang="scss">
.navbar {
  width: 100%;
}
</style>

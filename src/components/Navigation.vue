<template>
  <div>
    <v-navigation-drawer
      v-model="drawer"
      app
      temporary
      dark
      
    >
      <v-list>
        <v-list-item>
          <v-list-item-avatar>
            <img src="@/assets/fotocv2.jpg" alt="Logo" />
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title class="title">Bienvenidos</v-list-item-title>
            <v-list-item-subtitle>Portfolio web</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-divider />

      <v-list dense>
        <v-list-item
          v-for="([icon, text, link], i) in items"
          :key="i"
          link
          @click="$vuetify.goTo(link)"
        >
          <v-list-item-icon class="justify-center">
            <v-icon>{{ icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="subtitile-1">{{
              text
            }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      :color="color"
      :flat="flat"
      dark
      class="px-15"
      :class="{ expand: flat }"
    >
      <v-toolbar-title>
        <v-list-item-title class="title">Bienvenidos</v-list-item-title>
      </v-toolbar-title>
      <v-spacer />
      <v-app-bar-nav-icon
        @click.stop="drawer = !drawer"
        class="mr-4"
        v-if="isXs"
      />
      <div v-else>
        <v-btn text @click="$vuetify.goTo('#home')">
          <span class="mr-2">Home</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#yo')">
          <span class="mr-2">Sobre mi</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#cursos')">
          <span class="mr-2">Capacitaciones</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#proyects')">
          <span class="mr-2">Practicas</span>
        </v-btn>
        <v-btn text @click="$vuetify.goTo('#contact')">
          <span class="mr-2">Cv</span>
        </v-btn>
        <v-btn rounded outlined text @click="$vuetify.goTo('#contacto')">
          <span class="mr-2">Contacto</span>
        </v-btn>
      </div>
    </v-app-bar>
  </div>
</template>

<style scoped>


.expand {
  height: 80px !important;
  padding-top: 10px;
}
</style>

<script>
export default {
  data: () => ({
    drawer: null,
    isXs: false,
    items: [
      ["mdi-home-outline", "Home", "#home"],
      ["mdi-information-outline", "Sobre mi", "#yo"],
      ["mdi-note", "Capacitaciones", "#cursos"],
      ["mdi-map", "Practicas", "#proyects"],
      ["mdi-face", "Cv", "#contact"],
      ["mdi-email-outline", "Contacto", "#contacto"],
    ],
  }),
  props: {
    color: String,
    flat: Boolean,
  },
  methods: {
    onResize() {
      this.isXs = window.innerWidth < 850;
    },
  },

  watch: {
    isXs(value) {
      if (!value) {
        if (this.drawer) {
          this.drawer = false;
        }
      }
    },
  },
  mounted() {
    this.onResize();
    window.addEventListener("resize", this.onResize, { passive: true });
  },
};
</script>

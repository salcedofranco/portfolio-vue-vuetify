<template>
  <v-app>
    <navigation :color="color" :flat="flat" />
    <v-main class="pt-0">
      <Header/>
      <SobreMi/>
      <Certificaciones/>
      <Proyectos/>
      <Cv/>
      <Contacto/>
      <Form/>
      
    </v-main>
    <v-scale-transition>
      <v-btn
        fab
        v-show="fab"
        v-scroll="onScroll"
        dark
        fixed
        bottom
        right
        color="secondary"
        @click="toTop"
      >
        <v-icon>mdi-arrow-up</v-icon>
      </v-btn>
    </v-scale-transition>
    <v-footer padless>
    <v-col
      class="text-center red lighten-1"
      cols="12"
    >
      {{ new Date().getFullYear() }} — <strong>Portfolio personal Franco Salcedo</strong>
    </v-col>
  </v-footer>
  </v-app>
</template>
<style scoped>
.v-main {
  
  background-attachment: fixed;
  background-position: center;
  background-size: cover;
  
  
}
</style>

<script>
import navigation from "./components/Navigation";

import Header from './components/Header';
import SobreMi from './components/SobreMi';
import Certificaciones from './components/Certificaciones';
import Proyectos from './components/Proyectos';
import Cv from './components/Cv';
import Contacto from './components/Contacto';
import Form from './components/Form';


import { mdiCardAccountDetails } from '@mdi/js';



export default {
  name: 'App',

  components: {
    navigation,
    Header, 
    SobreMi,
    Certificaciones,
    Proyectos,
    Cv,
    Contacto,
    Form
  },

  data: () => ({
    fab: null,
    color: "",
    flat: null,
  }),
  created() {
    const top = window.pageYOffset || 0;
    if (top <= 60) {
      this.color = "transparent";
      this.flat = true;
    }
  },
  watch: {
    fab(value) {
      if (value) {
        this.color = "secondary";
        this.flat = false;
      } else {
        this.color = "transparent";
        this.flat = true;
      }
    },
  },
  methods: {
    onScroll(e) {
      if (typeof window === "undefined") return;
      const top = window.pageYOffset || e.target.scrollTop || 0;
      this.fab = top > 60;
    },
    toTop() {
      this.$vuetify.goTo(0);
    },
  },
};
</script>

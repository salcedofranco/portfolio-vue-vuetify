<template>
<section id="proyects">
    <div class="svg-border-waves">
      <img src="~@/assets/tilt3.svg" />
    </div>
<v-container>
  <v-row align="center" justify="center">
    <v-col class="subtitulo pt-5" cols="12">
      <h1 class="display-2 font-weight-white text-center deep-purple--text text-xl-h4">Practicas y Proyectos</h1>   
    </v-col>
  </v-row>

  <v-row class="fila">
    <v-col class="1" lg="4" >
      <v-card class="mx-auto" max-width="400">
        <v-img
          class="white--text align-end"
          height="200px"
          src="@/assets/red-bici.jpg"
          >
          <v-card-title></v-card-title>
        </v-img>
        <v-card-title class="pb-0">RED DE BICICLETAS</v-card-title>
        <v-card-text class="text--primary">
          <div>Whitehaven Beach</div>
          <div></div>
        </v-card-text>

        <v-card-actions>
          <v-btn 
            color="orange" 
            text
            href="https://red-bicicletas-deploy.herokuapp.com/"> Ver proyecto
          </v-btn>

          <v-btn 
            color="black" 
            text
            href="https://github.com/salcedofranco/redBicicletasCoursera">Ir a Github
          </v-btn>
        </v-card-actions>

      </v-card>
    </v-col>

    <v-col class="2"  lg="4" >
      <v-card class="mx-auto" max-width="400">
        <v-img
          class="white--text align-end"
          height="200px"
          src="@/assets/imagenAgencia.jpg"
          >  
        </v-img>

        <v-card-title class="pb-0">AGENCIA DE VIAJES</v-card-title>

        <v-card-text class="text--primary">
      <div>Whitehaven Beach</div>

      <div></div>
      </v-card-text>

      <v-card-actions>
      <v-btn
        color="orange"
        text
        href="https://agencia-de-viajes-node.herokuapp.com/">Ver proyecto
      </v-btn>

      <v-btn
        color="black"
        text
        href="https://github.com/salcedofranco/AgenciaDeViaje-Udemy">Ir a Github 
      </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>

    <v-col class="3"  lg="4" >
      <v-card class="mx-auto" max-width="400">
        <v-img class="white--text align-end" height="200px" src="@/assets/imagenMovies1.jpg">
        </v-img>

        <v-card-title class="pb-0">APP INFO DE PELICULAS</v-card-title>

        <v-card-text class="text--primary">
        <div>Whitehaven Beach</div>
        <div></div>
        </v-card-text>

        <v-card-actions>
        <v-btn 
        color="orange" 
        text 
        href="https://tutorial-search-movies.herokuapp.com/">Ver proyecto
        </v-btn>

        <v-btn 
        color="black" 
        text 
        href="https://github.com/salcedofranco/appSearchMovie">Ir a Github
        </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>

    <v-col class="4"  lg="6" >
      <v-card class="mx-auto" max-width="400">
        <v-img class="white--text align-end" height="200px" src="@/assets/imagenMovies1.jpg">
        </v-img>

        <v-card-title class="pb-0">APP INFO DE PELICULAS</v-card-title>

        <v-card-text class="text--primary">
        <div>Whitehaven Beach</div>
        <div></div>
        </v-card-text>

        <v-card-actions>
        <v-btn 
        color="orange" 
        text 
        href="https://tutorial-search-movies.herokuapp.com/">Ver proyecto
        </v-btn>

        <v-btn 
        color="black" 
        text 
        href="https://github.com/salcedofranco/appSearchMovie">Ir a Github
        </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>

  </v-row>
</v-container>

</section>
</template>

<script>
    export default {
        name: 'Slider',
    }
</script>

<style scoped>

#proyects{
    background-color: #1e1f20;
}

.subtitulo {
  padding-top: 0;
  padding-bottom: 2rem;
  filter: drop-shadow(0px 0px 2px #bf09ec);
}

.fila{
    padding-bottom: 3em;
}

.svg-border-waves .v-image {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 3rem;
  width: 100%;
  overflow: hidden;
}
#hero {
  z-index: 0;
}
.svg-border-waves img {
  
  margin-bottom: -8px;
  z-index: -1;
}

</style>
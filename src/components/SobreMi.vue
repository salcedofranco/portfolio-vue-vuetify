<template>
<section id="yo">
  
<v-container fluid class="container pa-0">

      <v-col class="subtitulo pt-5">
        <h1 class="display-2 font-weight-white text-center light-green--text pt-0">Sobre mi</h1>
      </v-col>

    <v-row class="fila" align="center" justify="center">
        <v-col class="foto" cols="11" sm="6" md="4" xs="11" lg="4">
          <v-img  src="@/assets/foto-franco.jpg"  style="border-radius:50%;" max-width="350px"></v-img>
        </v-col>

        <v-col class="texto" cols="12" sm="6" md="8" xs="12" lg="8" >
          <h3 class="pa-5 white--text text-subtitle-1">Hola, 
           me llamo Franco Salcedo, soy de Mendoza - 
            Argentina y hace ya un tiempo que me anime a meterme en el mundo de la programación que tanto me gusta, desde entonces he tratado de estar en constante aprendizaje, ya sea con cursos presenciales, como también de forma autodidacta, además consulto y formo parte de algunas comunidades de desarrolladores en discord y slack que me ayudan a resolver problemas junto a mi mejor compañero (google).
            Actualmente estoy comenzando a ver Vue.js y terminando un curso de Javascript dictado por IDITS Mendoza y Node.js online en Coursera.
            Fuera del ambito del software lo que más me gusta es estar en familia, juntarme con amigos, jugar al futbol, compartir asados y ver series.</h3>  
        </v-col>

    </v-row>


</v-container>

</section>
</template>

<script>
  export default {
    name: 'SobreMi',
    
  }
</script>

<style scoped>

#yo{
 background-color:#1e1f20; 
}

.fila{
      display: flex;
    flex-wrap: wrap;
    flex: 1 1 auto;
    margin-right: 0;
    margin-left: 0px;
}

.subtitulo {
  padding-top: 0;
  padding-bottom: 2rem;
  filter: drop-shadow(0px 0px 2px #00ff15);
}


.foto{
  display: grid;
  align-items: center;
  justify-content: center;
  padding-bottom: 0;
  margin-bottom: 0;
  padding: 2
}

.texto{
  display: grid;
  align-items: center;
  justify-content: center;
  padding-top: 1rem;
  padding-bottom: 0;
  margin-bottom: 0;

  border-left: 4px solid rgb(11, 245, 3);

  
  
  
}


.container {
  padding-bottom: 0;
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
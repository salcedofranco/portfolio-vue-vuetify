<template>

  <section id="cursos">
    <div class="svg-border-waves">
      <img src="~@/assets/tilt1.svg" />
    </div>

    <v-container class="container">
      
     
    
       
    <v-row align="center" justify="center">
          <v-col class="subtitulo" cols="12">
            <h1 class="display-2 font-weight-white text-center orange--text text-xl-h4">Capacitaciones</h1>   
          </v-col>
    </v-row>

        <v-row wrap class="certificado" align="center" justify="center">
          <v-col class="columnas" cols="12" lg="4" sm="6" md="4" xs="12" >
          <a href="https://imgfz.com/i/4i0rnbF.jpeg" target="blank"><v-img class="img"  src="@/assets/coursera.jpg"></v-img></a>
          </v-col>

          <v-col class="columnas" cols="12" lg="4" sm="6" md="4" xs="12" >
          <a href="https://imgfz.com/i/Baf9Vli.jpeg" target="blank"><v-img class="img"  src="@/assets/nodeComIt.jpg"></v-img></a>
          </v-col>

          <v-col class="columnas" cols="12" lg="4" sm="6" md="4" xs="12" >
          <a href="https://imgfz.com/i/uLQkCtF.jpeg" target="blank"><v-img class="img"  src="@/assets/certificadoYpf.jpg"></v-img></a>
          </v-col>

          <v-col class="columnas" cols="12" lg="4" sm="6" md="4" xs="12" >
          <a href="https://imgfz.com/i/9QadBki.jpeg" target="blank"><v-img class="img"  src="@/assets/certificadoPhp.jpg"></v-img></a>
          </v-col>

          <v-col class="columnas" cols="12" lg="4" sm="6" md="4" xs="12" >
          <a href="https://imgfz.com/i/WcInsNS.jpeg" target="blank"><v-img class="img"  src="@/assets/certificadoScrum.jpg"></v-img></a>
          </v-col>

          <v-col class="columnas" cols="12" lg="4" sm="6" md="4" xs="12" >
          <a href="https://imgfz.com/i/75gCWUe.jpeg" target="blank"><v-img class="img"  src="@/assets/certificadoJavascript.jpg"></v-img></a>
          </v-col>

          
        </v-row>
      </v-container>
    
    </section>
</template>

<script>

    export default {
        name: 'Certificaciones',
         
    }
    
</script>



<style scoped>

#cursos{
  background-color: black;
  
}

.container{
  padding-top:0 ;
}

.subtitulo {
  padding-top: 0;
  padding-bottom: 2rem;
  filter: drop-shadow(0px 0px 2px #ff9100);
}

@media (max-width: 339px) {
    .subtitulo h1 {
      font-size: 40px !important;
    
  }
}

.columnas a{
  display: grid;
  justify-content: center;
  align-items: center;
  border-radius: 40%;
  
  
}

.columnas .img{
  border-radius: 5%;
  padding-bottom: 0;
}

.certificado {
  display: flex;
  flex-wrap: wrap;
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
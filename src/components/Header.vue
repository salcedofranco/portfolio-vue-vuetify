<template>
    <section id="home">
        <v-container fluid> 
            <v-parallax class="imagenHeader" dark src="@/assets/imagenHeader.jpg" height="650">
                <v-row align="center" justify="center">
                    <v-col>
                        <h1 class="display-3 font-weight-bold text-center text-uppercase">Franco Salcedo</h1>
                        <h1 class="display-2 font-weight-white text-center green--text">
                            Desarrollador de software junior
                        </h1>
                        
                    </v-col>
                    
                </v-row>
                 
            <div class="svg-border-waves">
                <img src="~@/assets/headersvg.svg" />
            </div>
            </v-parallax>
          
        </v-container>
       
    </section>
</template>

<script>
    export default {
        name: 'Header', 
    }
</script>

<style scoped>

.container{
    padding: 0;
}


.svg-border-waves img {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  margin-bottom: -2px;
  z-index: -1;
}



</style>
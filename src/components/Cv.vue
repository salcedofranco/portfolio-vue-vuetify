<template>
    <section class="pb-5" id="contact">
        <div class="svg-border-waves">
      <img src="~@/assets/tilt1.svg" />
    </div>
         
        <v-container class="container">
             <v-row class="mb-5" align="center" justify="center">
                 <v-col class="subtitulo mt-5 mb-5 " cols="12">
                    <h1 class="display-2 font-weight-white text-center red--text text-xl-h4">Curriculum</h1>   
                </v-col>
            </v-row >
            <v-row class=" mt-5">
                
                <v-col class="columnas" md="6">
                    <v-btn color="blue" dark icon href="https://i.ibb.co/F8x6KfN/CV-Franco-Salcedo-ult.jpg" target="_blank">
                        <v-icon large color="blue" style="font-size:120px">person</v-icon>
                    </v-btn>
                    <h3 class="blue--text mt-6">Ver C.V.</h3>
                </v-col>

                <v-col class="columnas" md="6">
                    <v-btn color="red" dark icon href="https://www.pdfhost.net/index.php?Action=DownloadFile&id=dcf0acffa8c3f62897560601d388cab3" target="_blank">
                        <v-icon large color="red" style="font-size:120px">mdi-cloud-download</v-icon>
                    </v-btn>
                    <h3 class="red--text mt-6 ">Descargar C.V.</h3> 
                </v-col>
            </v-row>
        </v-container>
        
    </section>
</template>

<script>
    export default {
        name: 'Cv',
        
    }

    
</script>

<style scoped>

.group {
  display: flex;
  flex: 1;
  justify-content: space-around;
}

#contact{
    background-color: black;
}

.container{
  padding-top:0 ;
  padding-bottom: 0;
}

.subtitulo {
  padding-top: 0;
  padding-bottom: 0;
  filter: drop-shadow(0px 0px 2px #ff0000);

}

.columnas{
    display: flex;
   align-items: center;
    justify-content: center;
    
    flex-wrap: wrap;
    flex-direction: column;
}

.svg-border-waves .v-image {
  position: absolute;
  bottom: 0;
  left: 0;
  height: 3rem;
  width: 100%;
  overflow: hidden;
}




</style>
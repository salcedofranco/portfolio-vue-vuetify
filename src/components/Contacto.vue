<template>
    <section id="contacto" >
        <div class="svg-border-waves">
      <img src="~@/assets/tilt3.svg" />
    </div>
        <v-container>
              <v-row align="center" justify="center">
                <v-col class="subtitulo pb-0" cols="12">
                    <h1 class="display-2 font-weight-white text-center text-xl-h4">Contacto</h1>   
                </v-col>
            </v-row>

            <v-row>
                <v-col cols="12" xs="12" md="12" lg="6"   > 
                    <mdb-container>
                            <mdb-row>
                                <mdb-col size="12" class="text-center mb-5">
                    <v-form class="formu" name="simple-form" method="POST" data-netlify="true" data-netlify-honeypot="bot-field">
                        <p>
                            <input type="hidden" name="form-name" value="simple-form" />
                        </p>

                        

                                    <!--<mdb-modal-header class="primary-color red-text">
                                     <h4 class="title"><fa class="fas fa-pencil-alt" /> Contact form</h4> 
                                    </mdb-modal-header>-->

                                    <mdb-modal-body class="grey-text">
                                    <mdb-input type="text" name="name" size="sm" label="Your name" icon="user" group  validate error="wrong" success="right"/>
                                    <mdb-input type="email" name="email" size="sm" label="Your email" icon="envelope" group  validate error="wrong" success="right"/>
                                    <mdb-textarea name="message" size="sm"  :rows="2" label="Your message" icon="pencil"/>
                                    </mdb-modal-body>
                                    <mdb-modal-footer>
                                    <!--<mdb-btn color="secondary" @click.native="showModal = false">Close</mdb-btn>-->
                                    <mdb-btn color="primary" tipe="submit">Enviar</mdb-btn>
                                    </mdb-modal-footer>
                               
                    </v-form> 
                    </mdb-col>
                            </mdb-row>
                        </mdb-container>

                </v-col>

                <v-col class="redes" cols="12" xs="12" md="12" lg="6">
                    <v-btn  color="light-blue" dark icon href="https://www.linkedin.com/in/francosalcedodev/" target="_blank">
                        <v-icon large color="blue" style="font-size:110px">mdi-linkedin</v-icon>
                    </v-btn>
                    

                    <v-btn  color="light-green" dark icon href="https://api.whatsapp.com/send/?phone=5402616590084&text&app_absent=0" target="_blank">
                        <v-icon large color="light-green" style="font-size:110px">mdi-whatsapp</v-icon>
                    </v-btn>
                    

                    <v-btn  color="red accent" dark icon href="mailto:fcedo13@gmail.com" target="_blank">
                        <v-icon large color="red" style="font-size:110px">mdi-gmail</v-icon>
                    </v-btn>
                    

                </v-col>
            </v-row>


        </v-container>
        
    </section>
</template>

<script>
  import { mdbContainer, mdbRow, mdbCol, mdbInput, mdbTextarea, mdbBtn, mdbIcon,mdbModalBody, mdbModalFooter } from 'mdbvue';
  export default {
    name: 'FormsPage',
    components: {
      mdbContainer,
      mdbRow,
      mdbCol,
      mdbInput,
      mdbTextarea,
      mdbBtn,
      mdbIcon
      
    },
    data() {
      return {
        showModal: false
      };
    }
  }
</script>

<style  scoped>

#contacto{
    background-color:#f1f1f1;
}

.subtitulo {
  padding-top: 0;
  padding-bottom: 2rem;
  color: #141414;
  filter: drop-shadow(0px 0px 2px #000000);

}

.sppb-form-control:focus
    {
    color: red !important;
}

.redes{
    display: flex;
    flex-wrap: wrap;
    align-content: center;
    justify-content: space-evenly;
    align-items: center;
    flex-direction: row;
    
    
}

.redes .v-btn{
    margin: 2em;
}


@media (max-width: 340px) {
    .redes .v-icon {
      font-size: 95px !important;
  }
}


</style>
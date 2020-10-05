<template>
    <section id="contacto">
        <div class="svg-border-waves">
      <img src="~@/assets/tilt3.svg" />
    </div>
        <v-container>
              <v-row align="center" justify="center">
                <v-col class="subtitulo" cols="12">
                    <h1 class="display-2 font-weight-white text-center blue--text text-xl-h4">Contacto</h1>   
                </v-col>
            </v-row>

            <v-row>
                <v-col cols="12" xs="12" md="12" lg="6"   > 
                    <v-form class="formu pa-1" name="contact" netlify>
                        <v-text-field
                            solo
                            v-model="name"
                            :counter="10"
                            :rules="nameRules"
                            label ="Name"
                            required
                            input type="text"
                            name="name"
                        ></v-text-field>

                        <v-text-field
                            solo
                            v-model="email"
                            :rules="emailRules"
                            label="E-mail"
                            required
                        ></v-text-field>

                        <v-textarea
                            solo class="light-red"
                            counter
                            label="Text"
                            :rules="rules"
                            name="message"
                            placeholder="Hola, desde aca podes enviarme un mensaje!"
                        ></v-textarea>

                        <p>
                    <button class="ma-2" outlined color="indigo" type="submit">Send</button>
                    </p>

                    <v-btn class="ma-2" outlined color="indigo" type="submit"> enviar Button
                    </v-btn>

                    </v-form>


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
    export default {
        data: () => ({
      rules: [
          v => !!v || 'Mensaje is required',
          v => v.length <= 300 || 'Max 300 caracteres'
          ],
      

      valid: false,
      name: '',
      nameRules: [
        v => !!v || 'Name is required',
        v => v.length <= 10 || 'Name must be less than 10 characters',
      ],
      
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+/.test(v) || 'E-mail must be valid',
      ],
    }),
  
    }
</script>

<style  scoped>

#contacto{
    background-color:#1e1f20;
}

.subtitulo {
  padding-top: 0;
  padding-bottom: 2rem;
  filter: drop-shadow(0px 0px 2px #008cff);

}

.redes{
    display: flex;
    flex-wrap: wrap;
    align-content: center;
    justify-content: space-evenly;
    align-items: center;
    flex-direction: row;
    background-color:#1e1f20;
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
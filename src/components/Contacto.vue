<template>
    <section id="contacto" >
        <div class="svg-border-waves">
          <img src="~@/assets/tilt3.svg" />
        </div>
        <v-container>
              <v-row align="center" justify="center">
                <v-col class="subtitulo" cols="12">
                    <h1 class="display-2 font-weight-white text-center text-xl-h4">Contacto</h1>   
                </v-col>
            </v-row>

            <v-row>
                <v-col cols="12" xs="12" md="12" lg="6"   > 
                    
                   <v-form  ref="form" v-model="valid" lazy-validation name="simple-form" method="POST" data-netlify="true" data-netlify-honeypot="bot-field">
        <input type="hidden" name="form-name" value="simple-form" />
      <p>
        <label> <input type="hidden" name="form-name" value="simple-form" /></label>   
      </p>
      <p>
        <!--<label>Your Name: <input type="text" name="name" /></label>-->
        <v-text-field
        solo
            type="text"
            name="name"
            label="Nombre:"
            
            v-model="name"
            :counter="10"
            :rules="nameRules"
            required
        ></v-text-field>   
      </p>
      <p>
        <!--<label>Your Email: <input type="email" name="email" /></label>-->
        <v-text-field
        solo
            type="email"
            name="email"
            label="Email:"

            v-model="email"
            :rules="emailRules"
            required
            
        ></v-text-field>
      </p>
      <p class="mb-0">
        <!--<label>Message: <textarea name="message"></textarea></label>-->
        <!--<label>Message: <mdb-textarea type="textarea" name="message" :rows="2" icon="pencil"/></label>-->
        <v-textarea
        class="mb-0"
          solo
          name="message"
          label="Desde acá podes enviarme un mensaje:"

          v-model="textarea"
          :rules="textareaRules"
        ></v-textarea>
      </p>
      <p>
        <!--<button type="submit">Send</button>-->
        <v-btn
          :disabled="!valid"
          class="ma-2"
          outlined
          color="#64DD17"
          type="submit"
          @click="validate"
        >
          Enviar
        </v-btn>
       <v-btn
      color="error"
      outlined
      class="mr-4"
      @click="reset"
    >
      Limpiar
    </v-btn>
      </p>
      <hr>
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
        name: 'Contacto',

        data: () => ({
      valid: true,
      name: '',
      nameRules: [
        v => !!v || 'Name is required',
        v => (v && v.length <= 10) || 'Name must be less than 10 characters',
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
      textarea: '',
      textareaRules: [
        v => v.length <= 200 || 'Max 200 characters',
        v => v.length >= 25 || 'Minimo 25 characters',
        
        
      ],
      
    }), 

    methods: {
      validate () {
        this.$refs.form.validate()
      },

      submit () {
        this.$refs.form.validate()
      },

      reset () {
        this.$refs.form.reset()
      },
    }

    }
</script>

<style  scoped>

#contacto{
    background-color:#272727;
}

.subtitulo {
  padding-top: 0;
  padding-bottom: 2rem;
  color: #f3f3f3;
  filter: drop-shadow(0px 0px 2px #ffffff);

}


.redes{
    display: flex;
    flex-wrap: wrap;
    align-content: center;
    justify-content: space-evenly;
    align-items: center;
    flex-direction: row;
    margin-top:2rem ;
    margin-bottom:3rem ;
    
    
}

.redes .v-btn{
    margin: 2em;
}


@media (max-width: 340px) {
    .redes .v-icon {
      font-size: 75px !important;
  }
}


</style>
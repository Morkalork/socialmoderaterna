<template>
  <v-container mt-5>
    <v-stepper v-model='testStep'>
      <v-stepper-header>
        <v-stepper-step :complete='testStep > 1' step='1'>Intressen</v-stepper-step>
        <v-divider></v-divider>
        <v-stepper-step :complete='testStep > 2' step='2'>Ideologi</v-stepper-step>
        <v-divider></v-divider>
        <v-stepper-step step='3'>Resultat</v-stepper-step>
      </v-stepper-header>
      <v-stepper-items>
        <v-stepper-content step='1'>
          <v-card class='mb-5 pa-5'
            color='red lighten-5'>
            <v-switch label='Jag gillar när det går bra!' v-model='form.interests.question1' color='blue' />
            <v-switch label='Jag uppskattar en välfungerande välfärdsmodell!' v-model='form.interests.question2' color='blue' />
            <v-switch label='Jag tycker att miljön är nice och bör bevaras!' v-model='form.interests.question3' color='blue' />
          </v-card>
          <v-btn color='red darken' @click='testStep = 2'>Nästa</v-btn>
          <v-btn flat >Avbryt</v-btn>
        </v-stepper-content>

        <v-stepper-content step='2'>
          <v-card class='mb-5 pa-5'
            color='blue lighten-5'>
            <v-switch label='Jag anser att man ska betala lagom med skatt!' v-model='form.interests.question1' color='blue' />
            <v-switch label='Jag vill att alla människor ska ha vård i Sverige!' v-model='form.interests.question2' color='blue' />
            <v-switch label='Jag tycker att om man kan hjälpa till så bör man!' v-model='form.interests.question3' color='blue' />

          </v-card>
          <v-btn color='red darken' @click='testStep = 3'>Nästa</v-btn>
          <v-btn flat @click='testStep = 1'>Tillbaks</v-btn>
        </v-stepper-content>

        <v-stepper-content step='3'>
          <v-card class='mb-5 pa-5'
            color='grey lighten-2'>
              <h1 class='my-3'>Grattis! Du är SocialModerat!</h1>
              <p>Vårt parti välkomnar dig och dina underbara åsikter! Alla får rösta på oss och ha en åsikt om vår framtida politik!</p>
              <p>Rösta på SocialModeraterna i valet!</p>
          </v-card>
          <v-btn color='red darken' @click='voted = true'>Rösta!</v-btn>
          <v-btn flat @click='testStep = 2'>Tillbaks</v-btn>
        </v-stepper-content>
      </v-stepper-items>
    </v-stepper>
    <v-snackbar v-model='voted'>Tack, glöm inte att rösta på riktigt i valet!</v-snackbar>
  </v-container>
</template>
<script>
export default {
  data () {
    return {
      voted: false,
      testStep: 0,
      form: {
        interests: {
          question1: true,
          question2: true,
          question3: true
        }
      }
    };
  }
};
</script>
<style scoped>

</style>


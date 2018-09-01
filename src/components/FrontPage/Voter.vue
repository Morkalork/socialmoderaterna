<template>
   <v-container grid-list-md text-xs-center pa-5 fluid :blue='leftToRight' lighten-5>
    <v-layout row wrap :class="{'pa-0': $vuetify.breakpoint.smAndDown, 'pa-5': $vuetify.breakpoint.mdAndUp}">
      <v-flex sm6 v-if='leftToRight'>
        <img :src='person.src' alt='Bild på en god väljare' />
      </v-flex>
      <v-flex sm6 text-lg-left>
        <h2 class='display-1 mb-3'>{{person.name}}, {{person.age}}</h2>
        <section>
          <p v-for='(text, index) in person.texts' :key='index' class='subheading'>{{text}}</p>
        </section>
      </v-flex>
      <v-flex sm6 v-if='!leftToRight'>
        <img :src='person.src' alt='Bild på en god väljare' />
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
export default {
  props: {
    person: Object,
    leftToRight: Boolean
  }
};
</script>
<style scoped>
img {
  height: 20rem;
}

@media only screen and (max-width: 720px) {
 img {
   height: auto;
   width: 90%;
   margin: 0 auto;
 } 
}

p {
  font-size: 1.2rem;
}
</style>

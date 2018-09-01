<template>
  <v-content>
    <v-parallax :src='imageSrc'>
      <h1 :class='{"display-1": $vuetify.breakpoint.smAndDown, "display-4": $vuetify.breakpoint.mdAndUp}'>
        <span class='sosse'>S</span>ocial<span class='borgare'>M</span>oderaterna
      </h1>
      <h2 class='headline mt-2 text-xs-left'><em>Vi varken vill eller kan,<br />
      vi har varken stolthet eller skam!</em></h2>
    </v-parallax>
    <plans />
    <constituency />
    <leaders />
    <test />
    <v-footer class='pa-3 mt-5'>
      <v-spacer></v-spacer>
      <div>Magnus Ferm &copy; {{year}}</div>
    </v-footer>
  </v-content>
</template>

<script>
import Splash from '@/assets/images/splash.jpg';
import Plans from './Plans';
import Constituency from './constituency';
import Leaders from './Leaders';
import Test from './Test';

export default {
  data () {
    return {
      imageSrc: Splash,
      year: new Date().getUTCFullYear()
    };
  },
  components: {
    plans: Plans,
    constituency: Constituency,
    leaders: Leaders,
    test: Test
  }
};
</script>

<!-- Add 'scoped' attribute to limit CSS to this component only -->
<style scoped>
.v-parallax {
  text-shadow: 0 0 1rem #000;
}
h1 {
  font-size: 4rem;
  text-align: right;
  margin-right: 3rem;
  border-bottom: 2px #fff solid;
}
.sosse {
  color: #ec1a33;
}

.borgare {
  color: #019cdb;
}
</style>

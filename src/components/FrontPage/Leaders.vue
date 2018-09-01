<template>
  <v-container text-xs-center mt-5>
    <v-layout row wrap>
      <v-flex xs12 mb-5>
        <h2 class='display-3 mb-2'>Våra stolta språkrör</h2>
        <section class='preamble subheading'>
          <p>För att få en så diversifierad ledning som möjligt har SocialModeraterna inte en men två(!) partiledare, eller språkrör som vi väljer att kalla det!</p>
          <p>Anders och Johan jobbar dag och natt för att bedriva vår politik i polemik med sig själva. Det gör att alla förslag redan är debatterade minst en gång innan de "kommer ut på marknaden", så att säga.</p>
          <p>Varför inte läsa lite med om våra stolta representanter? Nedan följer deras syn på Sverige och den politik SocialModeraterna har att erbjuda just Dig!</p>
        </section>
      </v-flex>
      <v-flex xs12 mt-5>
        <v-layout row wrap justify-center>
          <v-card v-for='leader in leaders' :key='leader.name' class='ma-2'>
            <v-card-media :src='leader.src' :height='cardHeight' alt='Partiledare'></v-card-media>
            <v-card-title primary-title>
              <div>
                <h3 class='display-1 mb-2'>{{leader.name}}</h3>
                <table class='mb-5'>
                  <tr>
                    <th>Roll:</th>
                    <td>{{leader.role}}</td>
                  </tr>
                  <tr>
                    <th>Intressen:</th>
                    <td>
                      <span>{{leader.interests.join(', ')}}</span>
                    </td>
                  </tr>
                  <tr>
                    <th>Förebild:</th>
                    <td>{{leader.rolemodel}}</td>
                  </tr>
                </table>
                <p v-for='(line, index) in leader.about' :key='index' class='subheading'>{{line}}</p>
              </div>
            </v-card-title>
          </v-card>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
import Leader1 from '@/assets/images/leader1.jpg';
import Leader2 from '@/assets/images/leader2.jpg';

export default {
  data () {
    return {
      cardHeight: '600px',
      leaders: [
        {
          src: Leader1,
          name: 'Johan Andersson',
          role: 'Språkrör',
          interests: ['Politik', 'Familjen', 'Glädje'],
          rolemodel: 'Astrid Lindgren',
          about: [
            'Jag började med politik för att jag ville förändra folks liv. Jag ville vara en positiv inverkan på den vardag som ibland kan vara så knepig att få ihop. Livspusslet som saknar en bit eller två.',
            'Min förebild träffade jag redan på som barn i böckerna om Emil och Pippi. Jag föreställde mig alltid hela landet som Bullerbyn, en plats där alla hjälpte alla och där alla fick plats. Det gör jag fortfarande och jag tror att det viktigaste för mig som politiker är att behålla det mänskliga perspektivet. Varje individ som jag har hjälpt är en seger, både för mig, individen och nationen som helhet!',
            'Mitt viktigaste mål är att bygga ett starkt Sverige där alla ges möjlighet att hjälpa till efter förmåga, ett land där alla barn får växa upp med glädje och vänskap, en plats där pensionärer kan ta en kopp kaffe med vänner och familj utan att behöva fundera på vad vaniljlängden kostade. Detta är vad jag tänker åstadkomma med SocialModeraterna, detta är mitt löfte!'
          ]
        },
        {
          src: Leader2,
          name: 'Anders Johansson',
          role: 'Språkrör',
          interests: ['Glädje', 'Politik', 'Familjen'],
          rolemodel: 'Selma Lagerlöf',
          about: [
            'Mitt steg in i politiken kom naturligt när jag gått ut skolan. Jag satte mig ner och funderade hur jag bäst kunde ha en positiv inverkan på alla människor runt om mig och bestämde mig för att det egentligen bara fanns politiken för mig. Det finns så många vars liv jag vill förbättra.',
            'Precis som min förebild, Selma Lagerlöf, står jag för kvinnors rösträtt och människans frihet har alltid varit central i min övertygelse. Jag kommer alltid att stå upp för de svaga, dem utan makt, dessa arbetets söner och döttrar vars leder förtvinar i varven runt om i landet.',
            'Mitt löfte, mina ansträngningar, min själ kommer jag att lägga ner för att se till att ingen i detta land ska behöva vara rädd, ingen ska tappa tro eller hopp och inte någon ska känna att de inte har mat för dagen. Tillsammans bygger vi gemenskaphet, förenade är vi starka. Detta är mitt löfte!'
          ]
        }
      ]
    };
  }
};
</script>
<style scoped>
.v-card {
  max-width: 400px;
}

.v-card__media__background {
  background-size: cover;
}

th,
td {
  text-align: left !important;
}

th {
  padding-right: 3rem;
}

.preamble {
  max-width: 40vw;
  margin: 0 auto;
}

@media screen and (max-width: 720px) {
  .preamble {
    max-width: 90vw;
  }
}
</style>

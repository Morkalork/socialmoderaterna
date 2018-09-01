<template>
  <v-container fluid grid-list-sm pa-5>
    <v-layout row wrap justify-center="">
      <v-card v-for='card in cards' :key='card.title' class='ma-2'>
        <v-card-media :src='card.src' :height='cardHeight'></v-card-media>
        <v-card-title primary-title>
          <div>
            <h3 class='headline'>{{card.title}}</h3>
            <p>{{card.description}}</p>
          </div>
        </v-card-title>
        <v-card-actions>
          <v-btn flat color='orange'>Läs mer</v-btn>
          <v-btn flat color='orange'>Dela</v-btn>
        </v-card-actions>
      </v-card>
    </v-layout>
  </v-container>
</template>

<script>
import Health from '@/assets/images/health.jpg';
import Economy from '@/assets/images/economy.jpg';
import Jobs from '@/assets/images/jobs.jpg';
import Equality from '@/assets/images/equality.jpg';
import Crime from '@/assets/images/crime.jpg';
import CyberCrime from '@/assets/images/cyber-crime.jpg';
import Referendum from '@/assets/images/referendum.jpg';
import Crisis from '@/assets/images/crisis.jpg';
import Military from '@/assets/images/military.jpg';
import School from '@/assets/images/school.jpg';
import Environment from '@/assets/images/environment.jpg';
import Trains from '@/assets/images/trains.jpg';

export default {
  data () {
    return {
      cardHeight: '200px',
      cards: [
        {
          src: Health,
          title: 'Vård & Omsorg',
          description:
            'Vi vill ha den bästa vården för så lite pengar som möjligt. Förstatliga hyrläkarnas bemanningsfirmor så att vi kan fakturera oss själva, bemanna vårdcentraler med oavlönad välvilja och hopp!'
        },
        {
          src: Economy,
          title: 'Ekonomi',
          description: 'Sänk skatten på arbete och pension, höj skatten på konsumtionsvaror. Detta gynnar en minskad konsumtion vilket är bra för miljön. Reparationer ska ske momsfritt!'
        },
        {
          src: Jobs,
          title: 'Jobb & Sysselsättning',
          description:
            'Alla måste inte jobba, men alla måste ha en sysselsättning. Annars blir vi sysslolösa och går med i organiserad brottslighet. 100% "sysselsättning" 2020!'
        },
        {
          src: Equality,
          title: 'Jämställdhet',
          description: 'Alla människor ska ha samma rättigheter och skyldigheter, oavsett omständigheter och klasstillhörigheter. Segregera trångsynthet och verklighet!'
        },
        {
          src: Crime,
          title: 'Brott & Straff',
          description:
            'Vi föreslår att ändra straffrabatten till en straffbonus, en typ av Bonus Malum: begår man fler än 5 brott, får man ett sjätte straff på köpet!'
        },
        {
          src: CyberCrime,
          title: 'Nätbrottslighet',
          description:
            'Nät-hat ska med nät-tjat bekämpas! Varje gång någon hatar på nätet så kommer vi att uppmuntra alla att beskriva hur ledsna de gör dem på Facebook/Twitter/Instagram!'
        },
        {
          src: Referendum,
          title: 'Demokrati',
          description: 'Vi förespråkar en stark folkrörelse och vill därför att staten en gång om året annordnar en folkomröstning med utvalda frågor för kommun, landsting och stat för att öka allas delaktighet i beslutsfattandet!'
        },
        {
          src: Crisis,
          title: 'Krisberedskap',
          description:
            'Brand? Storm? Ösregn? Utsläpp? Allt går att lösa med hjälp av JAS 39 Gripen och GBU-49 laserstyd bomber!'
        },
        {
          src: Military,
          title: 'Militär beredskap',
          description:
            'Vi föreslår att vi går med i NATO, sen lägger vi de 3% av landets BNP som vi måste lägga på vår militär på att utveckla JAS och låter danskj****n sköta resten av försvaret. Win-win!'
        },
        {
          src: School,
          title: 'Skola',
          description: 'En privat skola i statlig regi gagnar alla! Vi vill introducera begreppet "Furstelärare" för att få ordning och reda i skolorna!'
        },
        {
          src: Environment,
          title: 'Miljön',
          description: 'Vi introducerar stolt "Miljön-programmet", vi ska plantera en miljon träd om året för att kontra skogsbränder och pappersmasseindustrin!'
        },
        {
          src: Trains,
          title: 'Trafik',
          description: 'Vi arbetar för att introducera ett nationellt superbuss-nätverk från Luleå till Trelleborg! Tågen går ändå inte, lägg pengarna på det som funkar!'
        }
      ]
    };
  }
};
</script>

<style scoped>
.v-card__title {
  max-width: 25rem;
}

.v-card__actions {
  position: absolute;
  bottom: 0;
}

.v-card__title {
  padding-bottom: 3rem;
}
</style>
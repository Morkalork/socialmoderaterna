<template>
  <div>
    <voter :person='people[0]' :leftToRight='true' />
    <voter :person='people[1]' :leftToRight='false' />
    <voter :person='people[2]' :leftToRight='true' />
  </div>
</template>

<script>
import Voter from './Voter';
import Person1 from '@/assets/images/person1.jpg';
import Person2 from '@/assets/images/person2.jpg';
import Person3 from '@/assets/images/person3.jpg';

export default {
  data () {
    return {
      people: [
        {
          src: Person1,
          name: 'Jasmine Nilsson',
          age: '20',
          profession: 'Konditor',
          texts: [
            'Jag tror att det jag gillar med SocialModeraterna är deras inställning till nät-hat. Jag blir alltid så ledsen när jag ser folk nät-hata, men jag känner definitivt att jag som medborgare kan bidra med att nät-tjata. Jag brukar alltid skriva till mina vänner på facebook hur jag känner mig, nu har jag ytterligare en anledning till att göra det!',
            'Även det här om att fokusera på busstrafik tror jag starkt på, jag bor nära Stockholm så vi har inte direkt några fungerande tåg, men bussar hade ju varit jättetrevligt!'
          ]
        },
        {
          src: Person2,
          name: 'Boris Chrustovski',
          age: '26',
          profession: 'Kattvakt',
          texts: [
            'Som professionel kattvakt känner jag att ett medlemskap i NATO skulle göra mycket för landet, speciellt som både jag och min sambo ofta bekymrar oss om underfinansieringen av ett av landets största industriprojekt; JAS 39 Gripen. Här känner jag att SocialModeraterna tar ansvar för nationens flygvapens framtid.',
            'Tycker även om att man vill satsa mer på att bomba bort naturkatastrofer och andra nationella olägenheter. '
          ]
        },
        {
          src: Person3,
          name: 'Rut & Ragnar Rinketofta',
          age: '68 & 72',
          profession: 'Pensionärer',
          texts: [
            'Rut: När vi fick höra att det här partiet vill sänka skatten för pensionärer så blev vi så himla imponerade, det är allt vi behöver höra. Att de dessutom vill höja skatten på konsumtionsvaror låter jättebra, vi brukar inte handla så mycket och de här ungdomarna handlar ändå för mycket.',
            'Ragnar: Ja, jag såg en flicka på bussen prata i telefonen tills batteriet tog slut, sen tog hon upp en annan telefon och fortsatte samtalet där. Då tänkte jag på alla de där undersökningarna om att de här mojängerna ger en cancer och lade fingrarna i kors...',
            'Rut: Haha, ja halleda. Men allvarligt, en beskattning kan ju faktiskt rädda liv. SocialModeraterna verkar ha huvudet på skaft!'
          ]
        }
      ]
    };
  },
  components: {
    'voter': Voter
  }
};
</script>
<style scoped>
</style>

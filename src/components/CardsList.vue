<script>
import axios from 'axios';
import Card from './Card.vue'


export default{
  components:{
    Card,
},

  data(){
    return{
      Cards:[],                                 //  1- creo un array vuoto al'interno salvo la lista dei cards
    };
  },
  methods:{                                     //  2- faccio una funzione per scaricare e recuperare i dati dei cards
    fetchCards(){
      const url = "https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0"  // 3- salvo in variabile l'URL recuperato dal sito

      axios.get(url).then((response) => {       //  4- faccio la chiamata tramite axios ps. axios deve essere importato.
                                                // debugger;
                                                //  5- una volta recuperati i dati dal server, li salvo in una variabile nel data
        this.Cards = response.data.data;

      });
    },
  },
  mounted() {                                   //  6- invoco nel mounted la funzioen fetchcards
    this.fetchCards();
  },

};

</script>

<template>

 

  <div class="row row-col-2 row-col-lg-5  g-4">
                                                <!--   7- faccio il ciclo for per recuperare ogni singolo card   -->
    <div class="col" 
      v-for="singleCard in Cards" :key="singleCard.id"> 

      <Card :card="singleCard"></Card>
    </div>
  </div>



  <!-- 9- creo un componente per la card lo importo qua e lo dichiaro nel export defaulte poi lo uso nel html -->
  <!-- 10-  passo gli informazione al componente card tramite props nel export defaultin card.vue -->
  <!-- 11- devo passare il valore props nel template <card></card>  -->

</template>


<style lang="scss" scoped>

</style>
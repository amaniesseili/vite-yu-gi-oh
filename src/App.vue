<script >
import TheHeader from './components/TheHeader.vue';
import CardsList from './components/CardsList.vue';
import AdvancedFilters from './components/AdvancedFilters.vue';


export default {
    components: {
    TheHeader,
    CardsList,
    AdvancedFilters
},
    methods: {
      // fetchCards (nextUrl){

      // }
      // fetchNextPage(){

      // },
    },

    // perche mi da errore nel server???
    // watch: {
    //   "store.searchText": function (newsSearchText){
    //     this.Cards = [];
    //     this.fetchCards (
    //       https://db.ygoprodeck.com/api/v7/cardinfo.php?name=${{newSearchtext.toLowerCase()}}
    //     )
    //   }

    // }
}
</script>

<template>
  <TheHeader></TheHeader>

  <main> 
    <!-- advanced filters form -->
    <div class="container">
      <div class="row">
        <div class="col-3">
          <AdvancedFilters  @filters-submitted="onFiltersSubmitted"></AdvancedFilters>

        </div>
      </div>
    </div>
    
    <div class="container container-color mt-5">
  

      <CardsList></CardsList>


    </div>


  </main>


</template>

<style lang="scss">
main {
  background-color: #D9863D;
  padding-top: 1rem;
  padding-left: 4rem;
  padding-right: 4rem;
}

.container-color{
  background-color: white;
  

}

</style>

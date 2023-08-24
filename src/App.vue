<script >
import TheHeader from './components/TheHeader.vue';
import CardsList from './components/CardsList.vue';


export default {
    components: {
      TheHeader,
      CardsList

    }
}
</script>

<template>
  <TheHeader></TheHeader>

  <main> 
    <div class="container">
      ghjk

      <CardsList>

      </CardsList>


    </div>


  </main>


</template>

<style lang="scss">
main {
  background-color: #D9863D;
  padding-top: 4rem;
  padding-left: 4rem;
  padding-right: 4rem;
}

.container{
  background-color: white;
  

}

</style>

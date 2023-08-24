<script>
export default{
  props: {
    card: {
      type: Object,
      required: true,
    },
  },

};

</script>

<template>

        <div class="card h-100"> 
        <!--   8- recupero l'immagine nel :src  il nome e l'archetype-->
          <img :src="card.image_url" class="card-img-top" alt="..."> 
        <div class="card-body">
          
          <h3 class="card-title">{{card.name}}</h3>
          <h4 class="card-title">{{card.archetype}}</h4>
            
            <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
        </div>
      </div>

</template>


<style lang="scss" scoped>

</style>
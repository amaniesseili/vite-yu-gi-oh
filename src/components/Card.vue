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


        <div class="card h-100 "> 
          <!--   8- recupero l'immagine nel :src  il nome e l'archetype-->
          <img :src="card.card_images[0].image_url" class="card-img-top" alt="..."> 
        <!-- /////// perche nn funziona il d-flex neanche in css ?? ////// -->
          <div class="card-body d-flex flex-column ">  
            <h3 class="card-title">{{card.name}}</h3>
            <p class="card-text">{{card.archetype}}</p>
          </div>
      </div>

</template>


<style lang="scss" scoped>
.card-body{
  display: flex;
  flex-direction: column;
  background-color: #D9863D;
}

.card-title{
  color: white;
  font-size: 18px;
  text-align: center;
  
}
.card-img-top{
  min-width:200px;
  
}
.card-text{
  text-align: center;
}


</style>
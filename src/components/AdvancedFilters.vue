<script>
export default{
    data(){
    return{
      formData:{},
    };
  },


};
//-------------------------------------------------
/**import axios from 'axios'
export default{
  data() {
    return{
      selectedArchetype: "",
      archetypes: [],
(devo aggiungere anche l'array del cards??)
    };
  },
  methods:{
    fetchArchetypes () {
      const url = https://db.ygoprodeck.com/api/v7/archetypes.php

      axios.get(url).then((response) =>{
        this.archetypes = response.data.data;
      });
    },
  },

  mounted() {
    this.fetchArchetypes();
  },
  
}

*/
//---------------------------------------------------------------------


</script>

<template>
  <form action="" class="">
    

    <div class="row row-cols-2">
      <div class="col">
        <div class="mb-3">
          <label class="form-label"></label>
          <select class="form-select" v-model="formData.archetype">
            <option value=""></option>
            <option value="Alien">"Alien"</option>
            <option value="ABC">"ABC"</option>
            <option value="Ally of Justice">"Ally of Justice"</option>
            <option value="Ally of Justice">"ANoble Knight"</option>
            <option value="Ally of Justice">"Melodious"</option>
            <option value="Ally of Justice">"Tainted Treasure"</option>
            <option value="Archfiend">Archfiend</option> 
          </select>
        </div>
      </div>
    </div>
    
  </form>
<!-- -------------------------------------------------------- -->
<!-- <form action="" class="">
    

  <div class="row row-cols-2">
    <div class="col">
      <div class="mb-3">

        <label class="form-label"></label>
       
        <select class="form-select" v-model="selectedArchetype">
          
          <option value=""></option>

          <option 
            v-for="archetype in archetypes" 
            value="archetype_name"
            :key="archetype.id">{{archetype.archetype_name}}
          </option>

        </select>
      </div>
    </div>
  </div>
  
</form> -->




</template>


<style lang="scss" scoped>

</style>
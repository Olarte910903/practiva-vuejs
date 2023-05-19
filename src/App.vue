<script>
import Card from './components/Card.vue'

export default{
  data(){
    return{

      personaje:null
    }

  },
  components:{
    Card
  }, 
  mounted() {
    this.fetchCharacters();
  },
  methods:{
     fetchCharacters() {
      fetch('https://rickandmortyapi.com/api/character/1')
        .then(response => response.json())
        .then(data => {
          this.personaje = data;
        })
        .catch(error => {
          console.error(error);
        });
    }
  }
}
</script>

<template>
  <div class="container">

    <Card :nombrePersonaje="personaje.name" :imagenPersonaje="personaje.image" :descripcionPersonaje="personaje.origin.name"/>
  </div>
</template>

<style scoped lang="scss">
.container{
  background:green;
}
</style>

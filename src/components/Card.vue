<template>
  <div>
    <h1>{{ nombrePersonaje }}</h1>

    <img :src="imagenPersonaje" alt="">

    <p>{{ descripcionPersonaje }}</p>
  </div>
</template>

<script>
export default{
  props:{
    nombrePersonaje:{
      type: String,
      required: true,
    },
    imagenPersonaje:{

      type: String,
      required: true
    },
    descripcionPersonaje:{
      type: String,
      required: true
    }

  }
}
</script>

<style>

</style>
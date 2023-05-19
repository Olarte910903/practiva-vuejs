<script>
import StartButton from './components/StartButton.vue';
export default{

  data(){
    return {
      titulo: "Práctica Vue JS",
      elementos: ["Calcular", "Añadir", "Eliminar", "Borrar"],
      cantidad: 0
    }
  },
  components: {
    StartButton
  },
  methods: {
    sumar(){
      this.cantidad = this.cantidad + 1;
    },
    restar(){
      this.cantidad = this.cantidad - 1;
    },
    multiplicar(){
      this.cantidad = this.cantidad * 2;
    },
    borrar(){
      this.cantidad = 0;
    }
  }
}
</script>

<template>
  <div class="contenedor">
  <h1>{{ titulo }}</h1>
  <p>{{ cantidad }}</p>
  <div class="contenedor-botones">

    <StartButton :nombreVariable="elementos[2]" @click = "restar"/>
    <StartButton :nombreVariable="elementos[1]" @click = "sumar"/>
    <StartButton :nombreVariable="elementos[0]" @click = "multiplicar"/>
    <StartButton :nombreVariable="elementos[3]" @click = "borrar"/>
  </div>
</div>
</template>

<style scoped lang="scss">
.contenedor{
  $default-font: 'Oswald';
  h1{
    font-family:$default-font;
    color: green;
    }
    p{
      font-family: $default-font;
      font-size: 30px;
    }
  .contenedor-botones{
    display:flex;
    flex-direction: column;
    gap:20px;
  }
  }
</style>

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
@mixin flexAlineation($direction, $justify, $align){
  display:flex;
  flex-direction: $direction;
  justify-content: $justify;
  align-items: $align;
}
.contenedor{
  width: 700px;
  height: 400px;
  border-radius: 15px;
  box-shadow: 1px 1px 20px gray;
  @include flexAlineation(column,center ,center );
  background-color: antiquewhite
  ;
  $default-font: 'Oswald';
  h1{
    font-family:$default-font;
    color: green;
    font-size: 50px;
    padding: 0;
    margin: 0;
    }
    p{
      font-family: $default-font;
      font-size: 60px;
      padding: 0;
      margin: 30px;
    }
  .contenedor-botones{
    width:90vw;
    @include flexAlineation(row,center ,center );
    gap:30px;
  }
  }
</style>

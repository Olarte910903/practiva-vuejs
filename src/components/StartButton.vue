<template>
  <button>
    {{ nombreVariable }}
  </button>
</template>

<script>
export default{
  props: {
    nombreVariable: {
      default: "Botón"
    }
  }
}
</script>

<style scoped lang="scss">
 $default-font: 'Oswald';
  button{
    width: 120px;
    height: 50px;
    border-radius: 10px;
    background: purple;
    color:white;
    font-family: $default-font;
    font-size: 18px;
    border: none;
    &:hover{
      background: violet;
      color:black;
    }
  }
</style>
<template>
  <hr>
  <h3>Eventos de LifeCycle {{ time }}</h3>
  <a href="https://vuejs.org/guide/essentials/lifecycle.html">Mais exemplos</a>
</template>

<script>
export default {
  name: 'LifeCycle',
  data() {
    return { 
      time: ""
    }
  },
  created() {
    setTimeout(() => {
      this.time = "Criou"
    }, 1000);
  },
  mounted(){
    setTimeout(() => {
      this.time = "Montou"
    }, 2000);

  }
}
</script>
<style>
.fotos{
  width: 200px;
}
</style>
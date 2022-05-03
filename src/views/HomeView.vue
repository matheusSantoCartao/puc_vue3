<template>
  <div class="home">
    <img alt="Minha foto" src="../assets/foto.jpg" class="fotos">
    <HelloWorld msg="Minhas habilidades"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>

<style>
.fotos{
  width: 200px;
}
</style>
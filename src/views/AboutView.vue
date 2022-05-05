<template>
  <div class="about">
    <h1>Exemplos do que o vue é capaz</h1>
  </div>

  <PrimeiroComponente />
  <LifeCycle />
  <Diretivas />
  <Picture />
  <ManipulacaoArray />
  
  <hr>
  <ul>
    <li><a href="https://docs.emmet.io/cheat-sheet/">Emmet</a></li>
  </ul>
</template>

<script>
import PrimeiroComponente from '../components/PrimeiroComponente.vue'
import Diretivas from '../components/Diretivas.vue'
import LifeCycle from '../components/LifeCycle.vue'
import Picture from '../components/Picture.vue'
import ManipulacaoArray from '../components/ManipulacaoArray.vue'

export default {
  name: 'App',
  components: {
    PrimeiroComponente,
    LifeCycle,
    Diretivas,
    Picture,
    ManipulacaoArray
  }
}
</script>
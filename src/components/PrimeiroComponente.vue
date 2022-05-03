<template>
  <div>
    <hr>
    <h3>Mudança de dados rápida</h3>
    <p>Meu nome é {{ nome }} e sou um {{ profissao }}</p>
  </div>
</template>

<script>
export default {
  name: 'PrimeiroComponente',
  data() {
    return {
      nome: "Matheus",
      profissao: "Programador"
    }
  }
}
</script>
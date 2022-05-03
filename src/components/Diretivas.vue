<template>
  <hr>
  <h3>Diretivas e Eventos</h3>
  <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
  <p v-else>Estou em busca de novas oportunidades!</p>
  <p v-show="mostrar_email">Mande uma mensagem para: matheus@email.com</p>
  <button @click="showEmail">Mostrar e-mail</button>

  <ul>
    <li v-bind:key="index" v-for="(technology, index) in frontend_technologies">{{ technology }}</li>
  </ul>
</template>
<script>
export default {
  name: 'DiretivasComponent',
  data() {
    return {
      esta_trabalhando: false,
      mostrar_email: false,
      frontend_technologies: ["HTML", "CSS", "Vue"]
    }
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email
    }
  }
}
</script>
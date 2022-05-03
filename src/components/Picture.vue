<template>
  <img :src="avatar" :alt="descricao" class="fotos">
  <MudarImagem @mudar-imagem="mudarImagem" />
</template>
<script>
import MudarImagem from './MudarImagem.vue'

export default {
  components: { MudarImagem },
  name: 'PictureComponent',
  data() {
    return { 
      avatar: "./img/foto.jpg",
      descricao: "Minha foto"
    }
  },
  methods: {
    mudarImagem() {
      this.avatar = "https://media.istockphoto.com/photos/portrait-of-a-funny-goat-showing-tongue-picture-id1010812760"
    }
  }
}
</script>
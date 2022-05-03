<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      A coragem não é ausência do medo; é a persistência apesar do medo.
    </p>
    <h3>Soft Skills</h3>
    <div class="skill">
      <div>
        <img src="../assets/ss1.png" alt="">
        <p>O que não colocamos no curriculum</p>
      </div>
      <div>
        <img src="../assets/ss2.png" alt="">
        <p>Aptidões mentais, emocionais e sociais</p>
      </div>
      <div>
        <img src="../assets/ss3.png" alt="">
        <p>Facilmente Qualificáveis</p>
      </div>
    </div>
    <h3>Essential Links</h3>
    
    <div class="skill">
      <div>
        <img src="../assets/hs1.png" alt="">
        <p>O que colocamos no curriculum</p>
      </div>
      <div>
        <img src="../assets/hs2.png" alt="">
        <p>Aptidões técnicas, certificações, qualificações</p>
      </div>
      <div>
        <img src="../assets/hs3.png" alt="">
        <p>Facilmente Quantificáveis</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
a {
  color: #42b983;
}

.skill{
  display: flex;
  width: 100%;
  justify-content: space-evenly;
}

.skill div{
  width: 150px;
}
.skill div p{
  font-weight: bold;
}
</style>

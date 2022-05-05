<template>
  <hr>
  <h3>Maneiras legais de manipular um array EC6</h3>

  <input type="tel" v-mask="'##/##/####'" v-model="meuAniversario" />
  <button @click="dateBrToUsa">Tratamento de Data</button>
  <hr>
  <input type="tel" v-mask="'###.###.###-##'" placeholder="Digite seu cpf" />

  <input placeholder='Telefone'  v-mask="['(##) ####-####', '(##) #####-####']" />

  <div class="flexPosicionamento">
    <button @click="filter">Filter</button>
    <button @click="join">Join</button>
    <button @click="concatenar">Concat</button>
    <button @click="splice">splice</button>
    <button @click="find">Find</button>
    <button @click="variaveis">Variáveis</button>
    <button @click="removeElementoObjetoArray">Remover Elemento</button>
  </div>

 

</template>
<script>
import {mask} from 'vue-the-mask'
export default {
  name: 'ManipulacaoArray',
  directives: {mask},
  data() {
    return {
      esta_trabalhando: false,
      mostrar_email: false,
      meuAniversario: '',
      frontend_technologies: ["HTML", "CSS", "Vue"]
    }
  },
  methods: {
    variaveis(){

      //Teste de variáveis
      let variavelLet = 1
      if(variavelLet == 1){
        let variavelLet = 3
        console.log(variavelLet); // Saída 3
      }
      console.log(variavelLet); // Saída 1


      //If ternário
      let meuValor = true;

      let conteudo = (meuValor) ? 'deu certo': 'tente novamente'
      console.log(conteudo);
    },
    dateBrToUsa(){
      let arrayData = this.meuAniversario.split('/').reverse().join(['-']);
      console.log(arrayData);
    },
    find() {
      //Find simples
      let numeros = [ 3, 4, 7, 9 ];
      console.log(numeros.filter(element => element > 5)); // Output: 7
      
      //Find em obj
      let objFera = [ 
        { name: 'Apple', price: 3.55 },
        { name: 'Orange', price: 2.43 },
        { name: 'Papaya', price: 4.76 }
      ];
      const result = objFera.find(objFera => objFera.name === 'Apple');
      console.log(result); 
    },
    removeElementoObjetoArray() {
      let objFera = [ 
        { name: 'Apple', price: 3.55 },
        { name: 'Orange', price: 2.43 },
        { name: 'Papaya', price: 4.76 }
      ];
      const result = objFera.findIndex(objFera => objFera.name === 'Papaya');
      console.log(result); 

      if(confirm("Deseja remover?")){
        objFera.splice(result, 1);
        console.log(objFera)
      }
    },
    join() {
      const meuNome = ['Matheus', 'Costa', 'Pereira'];
      console.log(meuNome.join());
      console.log(meuNome.join([' ']));
    },
    concatenar() {
      const exatas = ['Calculo', 'Matemática', 'Física'];
      const humanas = ['Português', 'Filosofia', 'Cultura'];
      console.log(exatas.concat(humanas));
    },
    splice(){
      const elementos = ['DIV', 'TABLE', 'BODY'];
      console.log(elementos); 
      const removed = elementos.splice(1, 1);
      console.log(removed);
      console.log(elementos);
    },

  }
}
</script>
<style>
.flexPosicionamento{
  display: flex;
  width: 50%;
  justify-content: center;
}
.flexPosicionamento button{

}
</style>
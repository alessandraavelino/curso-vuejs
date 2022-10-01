<template>
  <div>
    <form id="app-form">
      <input type="text" v-model="input_name">
      <input type="submit" value="Enviar" v-on:click="submitForm">
    </form>
    <p>Meu nome é: {{ names }}</p>
    <p>Data binding: {{input_name}}</p>
    
    <table border="1">
      <tr>
          <th>Nome</th>
          <th>Idade</th>
          <th>Telefone</th>
        </tr>
        <tr>
          <td>{{usuario}}</td>
          <td>{{idade}}</td>
          <td>{{telefone}}</td>
        </tr>
    </table>
 
    <div @click="setColor('blue')" :style="`color: ${elefante}`" >
      i'm a div
    </div>
    <ul>
      <li v-for="{tecnologia, index} in tecnologias" v-bind:key="index">{{tecnologia}}</li>
      
    </ul>

    <ul>
      <li v-for="tecnologia in frontend" :key="tecnologia.id">
        {{ tecnologia.linguagem}}
      </li>
    </ul>

    <div :style = "`width: 400px; height: 400px; background-color: ${color}`">
    
    </div>
    <div :key="i" v-for="i in [1,2, 3, 4, 5]">
      {{i}}
    </div>
    <div v-if="false"> 
    hello
    </div>
    {{
      
      soma(conta.a, conta.b)
    }}
    <br>
    {{dog}}
    <br>
    {{dogs}}
    <br>
    {{text}}
    <NovoComponente />
    <LifeCycle />
    <HelloWorld ref="filho" anel="olha só" @on-teste="veja"/>
    <Usuario />
    <Form />
  </div>
</template>

<script>
import NovoComponente from './components/NovoComponente.vue';
import HelloWorld from './components/HelloWorld.vue';
import LifeCycle from './components/LifeCycle.vue';
import Usuario from './components/Usuario.vue';
import Form from './components/Form.vue';

export default {
  name: 'App',
  components: { HelloWorld, NovoComponente, LifeCycle, Usuario, Form },

  //componente do app

  //nome dado ao componente
  


  //informações q serão reativas ao layout
  data: () => ({
    elefante: "red",
    dog: "AUAU",
    dogs: ["labrador, pincher, caramelo"],
    conta: { a: 6, b: 3},
    color: 'red',
    names: "",
    text: "texto",
    input_name: "",
    tecnologias: ["python", "js", "jaava"],

    frontend: [
      {id: 1, linguagem: "html"},
      {id: 2, linguagem: "css"},
      {id: 3, linguagem: "vue"}
    ],



  }),

  //funções
  methods: {
    veja (){
      console.log("funcionou?")
    },
    setColor () {
      this.$refs.filho.digaoi()
    },
    soma (a, b){
      return a + b
      
    },

    submitForm(e) {
      e.preventDefault();

      this.names = this.input_name;
    }
    


  }


}
</script>

<style>
  div {
    color: red;
    text-align: center;
  }

</style>
<!--
v-if - condicional
v-for laços
@xxx - eventos
:xxx - dados a serem passados p div
v-show - condicional, responde ao componente da tela
-->
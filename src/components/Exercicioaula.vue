
<template>
    <!-- SINGLE FILE COMPONENT -->
    <div class="container">
      <h1>Calculadora IMC</h1>
      {{ peso }}
      <input type="number" v-model="peso" placeholder="Peso">
  
      {{ altura }}
      <input type="number" placeholder="Altura" v-model="altura">
      <button v-on:click="calcularimc()">Calcular</button>
      <!-- Resultado impresso -->
      <span>{{ resultado }}</span>
  
  
      <h2>PAR ou IMPAR</h2>
  
      <p>Informe o número</p>
      <input type="text" placeholder="Digite aqui" v-model="numero">
      <button @click="verificarnumero()">Verificar</button>
      <!-- Resultado impresso -->
      <span>{{ message }}</span>
    </div>
  </template>
  <!-- // Fica toda a logica de javaScript dentro do escript export default{} -->
  <script>
  
 
  export default {
    
    data() {
      // Somente variáveis são criadas no data(){}
       // sintaxe de objeto
      return {
        peso: 0,
        altura: 0,
        resultado: '',
        message: '',
        numero: 0
      }
    },
    // Funções são declaradas neste local
    methods: {
      calcularimc() {
        if (this.peso == 0 || this.altura == 0) {
          alert('Preencha todos os dados')
          return;
        }
        this.resultado = (this.peso / (this.altura ** 2)).toFixed(2);
      },
  
      verificarnumero() {
        if (this.numero % 2 === 0) {
          this.message = "O número é PAR";
        } else {
          this.message = "O número é IMPAR";
        }
      }
    }
  
  }
  </script>
  
  <style>
  .container {
    width: 100vw;
    height: 100vh;
    gap: 10px;
    padding: 20px;
    background-color: rgba(20, 181, 93, 0.298);
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  </style>
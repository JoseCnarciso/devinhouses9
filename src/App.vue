
<template>
  <!-- Faz a chamada do componente nesta área -->
  <Exercicioaula/>
</template>

<script>
// Importa o componente neste local
import Exercicioaula from './components/exercicioaula.vue'

export default {
  name: 'app',
  // Necessário listar neste local para poder utilizar a chamada no template
  components: {
    Exercicioaula
  }
}
</script>

<style>
</style>
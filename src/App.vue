<template>
  <div class="geral">
    <div class="cabecalho">
      <h1>Lista de Carros</h1>
    </div>
    <div class="lista">
      <ul>
        <li v-for="carro in carros"><strong>{{ carro.marca }}</strong> - <i>{{ carro.modelo }}</i></li>
      </ul>
    </div>
  </div>
</template>

<script>
import Carro from './servicos/carros';

export default {
  name: 'app',
  data () {
    return {
      carros: []
    }
  }
  ,mounted () {
    Carro.lista().then(dado => this.carros = dado.data);
  }
}
</script>

<style scoped>
  *{
    font-family: monospace;
  }
  li{
    font-size: 14pt;
  }
</style>

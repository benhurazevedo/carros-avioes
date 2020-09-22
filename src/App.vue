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
export default {
  name: 'app',
  data () {
    return {
      carros: [
        {marca: "VolksWagen", modelo: "Fusca"}
        ,{marca: "GM", modelo: "Corsa"}
        ,{marca: "Renault", modelo: "Clio"}
      ]
    }
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

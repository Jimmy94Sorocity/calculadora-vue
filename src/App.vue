<script setup>
  import { reactive } from "vue";
  import Cabecalho from "./components/Cabecalho.vue";
  import Formulario from "./components/Formulario.vue";
  import Resultado from "./components/Resultado.vue";

  const estado = reactive({
    resultado: 0,
  })

  const calculate = (numero1, numero2, operator) => {
    let resultado;

    switch (operator) {
      case "soma":
        resultado = numero1 + numero2;
        break;
      case "subtracao":
        resultado = numero1 - numero2;
        break;
      case "multiplicacao":
        resultado = numero1 * numero2;
        break;
      case "divisao":
        resultado = numero1 / numero2;
        break;
    }

    estado.resultado = resultado;
  }
</script>

<template>
  <div class="container">
    <Cabecalho />
    <Formulario
    :altera-conta="calculate"/>
    <Resultado :resultado="estado.resultado" />
  </div>
</template>

<style scoped>

</style>

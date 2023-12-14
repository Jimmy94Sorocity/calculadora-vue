<script setup>
  import { reactive } from "vue";
  import Cabecalho from "./components/Cabecalho.vue";
  import Formulario from "./components/Formulario.vue";
  import Resultado from "./components/Resultado.vue";

  const estado = reactive({
    numero1: 0,
    numero2: 0,
    resultado: 0,
    operator: "opcao",
  })

  const calculate = () => {
    const { operator } = estado;

    switch (operator) {
      case "soma":
        return resultado = numero1 + numero2;
      case "subtracao":
        return resultado = numero1 - numero2;
      case "multiplicacao":
        return resultado = numero1 * numero2;
      case "divisao":
        return resultado = numero1 / numero2;
    }
  }
</script>

<template>
  <div class="container">
    <Cabecalho />
    <Formulario
    :altera-conta="calculate()"
    :num1="evento => estado.numero1 = evento.target.value"
    :num2="evento => estado.numero2 = evento.target.value"/>
    <Resultado :resultado="evento => estado.resultado = evento.target.value"/>
  </div>
</template>

<style scoped>

</style>

<script setup>
  import { reactive } from "vue";
  import Cabecalho from "./components/Cabecalho.vue";
  import Formulario from "./components/Formulario.vue";
  import Resultado from "./components/Resultado.vue";

  const estado = reactive({
    numero1: "",
    numero2: "",
    resultado: "", 
  })

  const dividir = (num1, num2) => {
      this.num1 = estado.numero1;
      this.num2 = estado.numero2;
      if ( num1 / num2) {
        return estado.resultado;
      }
    }

    const multiplicar = (num1, num2) => {
      this.num1 = estado.numero1;
      this.num2 = estado.numero2;
      if ( num1 * num2) {
        return estado.resultado;
      }
    }

    const subtrair = (num1, num2) => {
      this.num1 = estado.numero1;
      this.num2 = estado.numero2;
      if ( num1 - num2) {
        return estado.resultado;
      }
    }

    const somar = (num1, num2) => {
      this.num1 = estado.numero1;
      this.num2 = estado.numero2;
      if ( num1 + num2) {
        return estado.resultado;
      }
    }
</script>

<template>
  <div class="container">
    <Cabecalho />
    <Formulario 
    :alteraConta="dividir"
    />
    <Resultado/>
  </div>
</template>

<style scoped>

</style>

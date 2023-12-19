<script setup>
    const props = defineProps(["alteraConta"]);
    let operator = "opcao";
    let numero1;
    let numero2;
</script>

<template>
    <form>
        <div class="row">
            <div class="col-md-4">
                <input required v-model="numero1" type="number" placeholder="Digite aqui o primeiro número" class="form-control">
            </div>
            <div class="col-md-4">
                <input required v-model="numero2" type="number" placeholder="Digite aqui o segundo número" class="form-control">
            </div>
            <div class="col-md-2">
                <select @change="props.alteraConta(numero1, numero2, operator)" v-model="operator" class="form-control">
                    <option value="soma">Soma</option>
                    <option value="subtracao">Subtração</option>
                    <option value="multiplicacao">Multiplicação</option>
                    <option value="divisao">Divisão</option>
                </select>
            </div>
        </div>
    </form>
</template>
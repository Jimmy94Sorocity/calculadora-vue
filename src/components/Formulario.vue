<script setup>
    const props = defineProps(["num1", "num2", "alteraConta"]);
</script>

<template>
    <form>
        <div class="row">
            <div class="col-md-4">
                <input required :value="props.num1" type="number" placeholder="Digite aqui o primeiro número" class="form-control">
            </div>
            <div class="col-md-4">
                <input required :value="props.num2" type="number" placeholder="Digite aqui o segundo número" class="form-control">
            </div>
            <div class="col-md-2">
                <select @change="props.alteraConta" class="form-control">
                    <option value="soma">Soma</option>
                    <option value="subtracao">Subtração</option>
                    <option value="multiplicacao">Multiplicação</option>
                    <option value="divisao">Divisão</option>
                </select>
            </div>
        </div>
    </form>
</template>
<script setup>
    const props = defineProps(["numero1", "numero2", "alteraConta"]);
</script>

<template>
    <form>
        <div class="row">
            <div class="col-md-4">
                <input required :value="props.numero1" type="number" placeholder="Digite aqui o primeiro número" class="form-control">
            </div>
            <div class="col-md-4">
                <input required :value="props.numero2" type="number" placeholder="Digite aqui o segundo número" class="form-control">
            </div>
            <div class="col-md-2">
                <select @keyup="props.alteraConta" class="form-control">
                    <option value="soma">Soma</option>
                    <option value="subtracao">Subtração</option>
                    <option value="multiplicacao">Multiplicação</option>
                    <option value="divisao">Divisão</option>
                </select>
            </div>
        </div>
    </form>
</template>
<script setup>
    const props = defineProps(["resultado"]);
</script>

<template>
    <ul class="list-group mt-4">
        <li class="list-group-item p-3">
            {{ props.resultado }}
        </li>
    </ul>
</template>
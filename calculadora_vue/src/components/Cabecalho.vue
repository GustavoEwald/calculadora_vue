<script setup>
const props = defineProps(['selecionado', 'primeiroValor', 'segundoValor'])
</script>

<template>
    <div class="cabecalho">
        <h1 class="titulo">Calculadora</h1>
        <span class="como-usar" v-if="!props.selecionado">Digite os dois números e selecione a operação</span>
        <span class="resultado" v-else>A {{ props.selecionado }} entre {{ props.primeiroValor }} e {{ props.segundoValor }} resulta em:</span>
    </div>
</template>

<style scoped>
.cabecalho {
    height: 150px;
}

.titulo {
    font-size: 48px;
    color: gold;
    text-align: center;
}

.como-usar {
    color: #fff;
    font-size: 30px;
}

.resultado {
    color: #fff;
    font-size: 24px;
}
</style>
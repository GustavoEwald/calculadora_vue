<script setup>
const props = defineProps(['selecionado', 'primeiroValor', 'segundoValor'])
</script>

<template>
    <div class="cabecalho">
        <h1 class="titulo">Calculadora</h1>
        <p class="como-usar" v-if="!props.selecionado">Digite os dois números e selecione a operação</p>
        <p class="resultado" v-else>A {{ props.selecionado }} entre {{ props.primeiroValor }} e {{ props.segundoValor }} resulta em:</p>
    </div>
</template>

<style scoped>
.cabecalho {
    min-height: 180px;

    @media (max-width: 576px){
        min-height: 150px;
    }
}

.titulo {
    font-size: 48px;
    color: gold;
    text-align: center;

    @media (max-width: 576px){
        font-size: 28px;
    }
}

.como-usar {
    color: #fff;
    font-size: 28px;
    display: block;
    text-align: center;
    margin-left: 5px;
    margin-right: 5px;

    @media (max-width: 576px){
        font-size: 24px;
    }
}

.resultado {
    color: #fff;
    font-size: 28px;
    text-align: center;
    margin: auto 8px;

    @media (max-width: 576px){
        font-size: 24px;
    }
}
</style>
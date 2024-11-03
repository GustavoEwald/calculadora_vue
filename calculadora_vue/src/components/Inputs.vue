<script setup>
const props = defineProps(['primeiroValor', 'segundoValor', 'opSelecionada'])
</script>

<template>
    <div class="container">
        <input class="numero" type="number" placeholder="00" @keyup="props.primeiroValor">
        <select class="operacao" @change="props.opSelecionada">
            <option value="" disabled selected>Operação</option>
            <option value="soma">+</option>
            <option value="diferença">-</option>
            <option value="divisão">&#247;</option>
            <option value="multiplicação">x</option>
        </select>
        <input class="numero" type="number" placeholder="00" @keyup="props.segundoValor">
    </div>
</template>

<style scoped>
    .container{
        display: flex;
        max-width: 400px;
        gap:5px;
        @media (max-width: 576px){
            flex-direction: column;
            gap:15px;
        }
    }

    .numero {
        border: none;
        border-bottom: 4px solid black;
        background-color: transparent;
        max-width: 100px;
        max-height: 40px;
        text-align: center;
        color: #fff;
        font-size: 24px;
        margin-left: 0;
        margin-right: 0;
    }

    .numero:focus {
        outline: none;
    }

    .numero::-webkit-inner-spin-button {
        appearance: none;
    }

    .operacao {
        border: none;
        background-color: transparent;
        max-width: 160px;
        height: 40px;
        font-size: 20px;
        appearance: none;
        color: gold;
    }

    .operacao::-webkit-inner-spin-button {
        appearance: none;
    }

    .operacao option {
        font-size: 20px;
        text-align: center;
        background-color: black;
        color: gold
    }
</style>
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
    }

    .numero {
        border: none;
        border-bottom: 4px solid black;
        background-color: transparent;
        width: 150px;
        height: 40px;
        text-align: center;
        color: #fff;
        font-size: 24px;
        padding: 15px;
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
        width: 160px;
        height: 40px;
        font-size: 30px;
        appearance: none;
        color: gold;
    }

    .operacao::-webkit-inner-spin-button {
        appearance: none;
    }

    .operacao option {
        font-size: 30px;
        text-align: center;
        background-color: black;
        color: gold
    }
</style>
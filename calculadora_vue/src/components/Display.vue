<script setup>
const props = defineProps(['opSelecionado', 'soma', 'dif', 'div', 'mult'])
</script>

<template>
    <div class="display">
        <span v-if="props.opSelecionado == 'soma'">{{ props.soma }}</span>
        <span v-else-if="props.opSelecionado == 'diferença'">{{ props.dif }}</span>
        <span v-else-if="props.opSelecionado == 'divisão'">{{ props.div }}</span>
        <span v-else-if="props.opSelecionado == 'multiplicação'">{{ props.mult }}</span>
        <span v-else>Selecione uma operacão</span>
    </div>
</template>

<style scoped>
.display {
    margin-top: 20px;
    width: 500px;
    height: 100px;
    background-color: transparent;
    border: 2px solid white;
    border-radius: 25px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.display span {
    color: #fff;
    font-size: 40px;
}
</style>
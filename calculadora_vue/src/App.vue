<script setup>
import { ref } from 'vue';
import Inputs from './components/Inputs.vue';
import Display from './components/Display.vue';
import Cabecalho from './components/Cabecalho.vue';

  const operacao = ref('');
  const num1 = ref(0);
  const num2 = ref(0);

  const ex = num1+num2;
  const soma = () => {return parseFloat(num1.value)+parseFloat(num2.value)};
  const dif = () => {return parseFloat(num1.value)-parseFloat(num2.value)};
  const div = () => {return parseFloat(num1.value)/parseFloat(num2.value)};
  const mult = () => {return parseFloat(num1.value)*parseFloat(num2.value)};

</script>


<template>
  <!-- <h3>{{ operacao }}</h3>
  <h2>{{ num1 }}</h2>
  <h2>{{ num2 }}</h2>
  <h3>{{ soma() }}</h3>
  <h3>{{ dif() }}</h3>
  <h3>{{ div() }}</h3>
  <h3>{{ mult() }}</h3> -->
  
  <div class="calculadora">
    <Cabecalho :selecionado="operacao" :primeiro-valor="num1" :segundo-valor="num2"></Cabecalho>
    <Display :op-selecionado="operacao" :soma="soma()" :dif="dif()" :div="div()" :mult="mult()" ></Display>
    <Inputs :primeiro-valor="evento=>num1=parseFloat(evento.target.value)" :segundo-valor="evento=>num2=parseFloat(evento.target.value)" :op-selecionada="evento=>operacao=evento.target.value"></Inputs>
  </div>
</template>


<style scoped>
  *{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  .calculadora{
    background-image: linear-gradient(rgb(88, 88, 119), rgb(88, 42, 88));
    width: 600px;
    height: 500px;
    display: flex;
    flex-direction: column;
    justify-content: start;
    align-items: center;
    border-radius: 25px;
  }

  .container{
    margin-top: 50px;
    display: flex;
    align-items:center;
    width: 500px;
    justify-content: space-between;
  }
</style>

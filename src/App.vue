<script setup>
import { reactive } from 'vue';


const filtros = reactive({
  filtro: 'soma',
  numberOne: 0,
  numberTwo: 0
})

function fazSoma(){
  return (parseInt(filtros.numberOne) + parseInt(filtros.numberTwo))
}

function fazSubtracao(){
  return (filtros.numberOne - filtros.numberTwo)
}

function fazMultiplicacao(){
  return (filtros.numberOne * filtros.numberTwo)
}

function fazDivisao(){
  return (filtros.numberOne / filtros.numberTwo)
}

const dizCalculo = () => {
  const {filtro} = filtros

  switch (filtro){
    case 'soma':
      return fazSoma()
    case 'subtração':
      return fazSubtracao()
    case 'multiplicação':
      return fazMultiplicacao()
    case 'divisão':
      return fazDivisao()
    
  }
}
</script>

<template>
  <header>
    <div class="container">
      <h1>
        Calculadora aritmética
      </h1>
    </div>
  </header>
  <div class="container">
    <form>
      <input @change="evento => filtros.numberOne = evento.target.value" type="number" class="number-one" placeholder="Digite um número">
      <select @change="evento => filtros.filtro = evento.target.value">
        <option value="soma">Soma</option>
        <option value="subtração">Subtração</option>
        <option value="multiplicação">Multiplicação</option>
        <option value="divisão">Divisão</option>
      </select>
      <input @change="evento => filtros.numberTwo = evento.target.value" type="number" class="number-two" placeholder="Digite um número">
    </form>
    <h2>{{dizCalculo()}}</h2>
  </div>
</template>

<style scoped>

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: sans-serif;
}

.container{
  max-width: 960px;
  width: 100%;
  margin: 0 auto;
}

header{
  background-color: #2B4257;
  text-align: center;
  padding: 32px 0px;
  color: #fff;
}

form{
  text-align: center;
  padding-top: 32px;
}

input::placeholder{
  text-align: center;
}

input,select{
  border-radius: 6px;
  height: 55px;
}

select{
  margin: 0px 32px;
}

h2{
  padding-top:2px ;
  margin: 40px auto;
  text-align: center;
  background-color: #2B4257;
  color: #fff;
  width: 100px;
  height: 30px;
  border-radius: 6px;
}

input{
  font-size: 20px;
}

input[data-v-7a7a37b1], select[data-v-7a7a37b1]{
  text-align: center;
  font-weight: bold;
}

@media (max-width:767px){
  input{
    width: 100px;
  }

  select{
    width: 50px;
  }
}

</style>

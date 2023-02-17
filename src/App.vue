<script setup>

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
      <input type="number" class="number-one" placeholder="Digite um numero">
      <select>
        <option value="soma">Soma</option>
        <option value="subtração">Subtração</option>
        <option value="multiplicação">multiplicação</option>
        <option value="divisão">Divisão</option>
      </select>
      <input type="number" class="number-two" placeholder="Digite um numero">
    </form>
    <h2>345</h2>
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

input,select{
  border-radius: 6px;
  height: 35px;
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
  width: 80px;
  height: 30px;
  border-radius: 6px;
}

</style>

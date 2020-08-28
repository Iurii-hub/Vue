<template>
  <!-- Homework Створити простий todolist В папці assests є скрін як приблизно має виглядати 
  ає бути масив тудушок, в інпуті вписуємо туду і пушимо в масив за допомогою кнопки Add. 
  Видаляємо тудушки за допомогою кнопки delete. Якщо тудушок більше 10 кнопка повинна сховатись. -->
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

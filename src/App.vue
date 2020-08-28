<template>
  <!-- Homework Створити простий todolist В папці assests є скрін як приблизно має виглядати 
  має бути масив тудушок, в інпуті вписуємо туду і пушимо в масив за допомогою кнопки Add. 
  Видаляємо тудушки за допомогою кнопки delete. Якщо тудушок більше 10 кнопка повинна сховатись. -->

  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>{{message}}</h1>
    
    <!-- <button v-on:click="increase">Increase</button>
    <button v-on:click="decrease">Decrease</button> -->

    <button v-on:click="counter++">Increase</button>
    <button v-on:click="counter--">Decrease</button>

    <p>{{counter}}</p>
    <p>{{counter > 10 ? "Greater than 10": "Smaller than 10" }}</p>
    <p>result: {{result()}}</p>



  </div>
</template>

<script>

export default {
  name: "App",

  data () {
    return {
      message: "HomeWork-1",
      counter: 0,
      // result: "",
    }
  },

  computed: {

  },

  methods: {

    result () {
      return this.counter > 10 ? "Greater than 10": "Smaller than 10";
    },

    // increase () {
    //   this.counter ++;
    //   this.result = this.counter > 10 ? "Greater than 10": "Smaller than 10";
    // },

    // decrease () {
    //   this.counter --;
    //   this.result = this.counter > 10 ? "Greater than 10": "Smaller than 10";
    // }

  }
}



</script>

<style>
</style>

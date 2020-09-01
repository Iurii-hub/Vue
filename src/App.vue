<template>
  <!-- Homework Створити простий todolist В папці assests є скрін як приблизно має виглядати 
  має бути масив тудушок, в інпуті вписуємо туду і пушимо в масив за допомогою кнопки Add. 
  Видаляємо тудушки за допомогою кнопки delete. Якщо тудушок більше 10 кнопка повинна сховатись. -->

  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>{{message}}</h1>

<!-- Homework begin -->

    <input type="text" v-model="todo">
    <button @click="add" v-if="arrayToDo.length <10">Add</button>
    <p v-else>No more allowed</p>

    <ul >
      <li v-for="(item, i) in arrayToDo" :key="i">
        <span>{{item}}</span>
        <button @click="remove(i)">Delete</button>
      </li>
    </ul>

<!-- Homework end -->

    <hr>
    <br>
    <br>
    <hr>

    <h2>{{message2}}</h2>
    
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

// <!-- Homework begin -->

export default {
  name: "App",

  data () {
    return {
      message: "HomeWork-1",
      todo : "",
      arrayToDo : [],

// <!-- Homework end -->

      message2: "Additional - counter",
      counter: 0,
      // result: "",
    }
  },

  computed: {

  },

// <!-- Homework begin -->

  methods: {
    add() {
      if (this.todo){
        this.arrayToDo.push(this.todo);
        this.todo = "";
      }
      else{
        alert('task not added');
      }
    },

    remove(i){
      this.arrayToDo.splice(i, 1);
    },

// <!-- Homework end -->

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

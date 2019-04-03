<template>
 <div id="app">
  <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo"/>
 </div>
</template>

<script>
 import Todos from './components/Todos.vue'

 export default {
  name: 'app',
  components: {
   Todos
  },
  data () {
   return {
    todos: [
     {
      id: 1,
      title: "Vue Intro",
      completed: false
     },
     {
      id: 2,
      title: "Instance dan property",
      completed: false
     },
     {
      id: 3,
      title: "Data binding",
      completed: false
     },
     {
      id: 4,
      title: "Computed properties",
      completed: false
     },
     {
      id: 5,
      title: "Conditional directives",
      completed: false
     },
     {
      id: 6,
      title: "Loop list",
      completed: false
     }
    ]
   }
  },
  methods: {
   deleteTodo(id) {
    this.todos = this.todos.filter(todo => todo.id !== id);
   }
  }
 }
</script>

<style>
 #app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
 }
</style>
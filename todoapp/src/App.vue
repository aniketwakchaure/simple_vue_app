<script>

import Todos from './components/Todos.vue'
import AddTodo from './components/AddTodo.vue'
export default{
  name:'app',
  components:{
    Todos,
    AddTodo
  },
  data(){
    return{
      todos:[
        {
        id:1,
        title:"ES6 classes",
        description:"modern javascript",
        status:false
        }
        
      ]
    }
  },
    methods:{
      addTodo(newTodoObj){
        //Combining old ones with the new one 
          this.todos = [...this.todos,newTodoObj]
      }
    }
}
</script>

<template>
  <div id="app">
    <Todos v-bind:todos="todos"/>
    <AddTodo v-on:add-todo="addTodo" />
  </div>
</template>
<style>

</style>



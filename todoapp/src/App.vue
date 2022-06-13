<script>
import Todos from './components/Todos.vue'
export default{
  name:'app',
  components:{
    Todos
  },
  data(){
    return{
      todos:[
        {id:1,name:"ES6 classes",status:false},
        {id:2,name:"Node classes",status:false},
        {id:3,name:"Typescript Classes",status:false},
        {id:4,name:"Vue classes",status: false}
      ]
    }
  }
}
</script>

<template>
  <div id="app">
    <Todos v-bind:todos="todos"/>
  </div>
</template>
<style>

</style>



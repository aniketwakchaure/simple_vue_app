<script>
import { isInDestructureAssignment } from '@vue/compiler-core'

  export default{
    data(){
        return{
          count:0,
          fname:"Aniket"
        }
    },
    //Methods
    methods:{
      increment(){
          this.count++
      }
    },
//Component API Life cycle Methods
    mounted(){
            console.log(`The initial count is ${this.count}`)
    }
  }


</script>

<template>
  <h1>First Web Component</h1>
  <button @click="increment">Count is :{{count}}</button>
  <p>{{fname}}</p>
  <h2>First Web Component</h2>
  <h3>First Web Component</h3>
  <h4>First Web Component</h4>
  <h5>First Web Component</h5>
  <h6>First Web Component</h6>
</template>

<style>
h1{
  color:brown
  }
 
</style>

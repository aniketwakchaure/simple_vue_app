<script>
import { v4 as uuidv4 } from 'uuid';

export default{
    name:'AddTodo',
    data(){
        return{
            title:"",
            description:""
        }
    },
    methods:{
        addTodo(event){
                event.preventDefault()
                const newTodoObj = {
                    id:uuidv4(),
                    title:this.title,
                    description:this.description,
                    status:false

                }
                this.$emit('addTodo',newTodoObj)
                this.title=""
        }
    }
}
</script>
<template>
    <div>
        <form @submit="addTodo">
            <input type="text" v-model="title" name="title"/>
            <input type="text" v-model="description" name="description"/>
            <button type="submit">Add</button>
        </form>
    </div>

</template>
<style></style>
<template>
    <div>
        <input @keyup.enter="addTodo" v-model='input'>
        <img :src = "img" width = '200' @click = "sayHellow" >
        <h1 v-if='todos.length === 0'>ничего нет</h1>
        <ul v-else>
            <li 
                @click='changeItem(item)' 
                :class= "{ active: item.completed}" 
                v-for="(item, index) in todos" 
                :key='index'
            >
                {{item.text}}
                <button @click="removeItem(index)" class='button'>x</button>
            </li>
        </ul>
        
    </div>
</template>




<script>
export default {
    name: 'Todo',
    props: {
        msg: String,
        img: String
    },
    data(){

        return {input: '',
        todos:[
            {text: "learn vue.js", completed: false},
            {text: "learn web", completed: true},
            {text: "пойти гулять", completed: false}
        ]    
        }
    },
    methods: {
        sayHellow(){
            alert('Hellow')
        },
        addTodo(){
           this.todos.push({text:this.input,completed: false})
           this.input =''
        },
        changeItem(item){
            item.completed = !item.completed

        },
        removeItem(index){
            this.todos.splice(index, 1)
        }
        
    },
}
</script>




<style>
    .h1{
        color: #40c8b0
    }
    .button{
        margin-left: 5px;
    }
    .active{
        text-decoration: line-through
    }
</style>
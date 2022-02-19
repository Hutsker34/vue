<template>
    <div>
        <h1 class ='h1'>{{input}}</h1>
        <input v-model = 'input'>
        <img :src = "img" width = '200' @click = "sayHellow" >
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
        return {input: ''}
    },
    methods: {
        sayHellow(){
            alert('Hellow')
        },
        
    },
}
</script>




<style>
    .h1{
        color: #40c8b0
    }
</style>
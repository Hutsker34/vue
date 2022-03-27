<template>
    <div>
        <input v-model="text" @keyup.enter="searchString" class="inp" placeholder="какая книга вас интересует?">
    </div>
</template>
<script>
export default {
    name: 'Search',
    props: {
        search: String,
        books: Array,

    },
    emits: ['search'],
    data(){
        return {
            text: "",
        }
    },
    methods: { 
        searchString(){
            let str = this.books.filter(item =>{
               return  this.exist(item , 'title') || this.exist(item , 'author')
            }) 
            this.$emit('search', str)
        },
        exist(item , field){
            if(this.text == ""){
                return false
            }
            return item[field].toUpperCase().indexOf(this.text.toUpperCase())>= 0
        }
    }
}
</script>
<style >
    .inp{
        width:200px;
        padding: 5px;
    }
</style>
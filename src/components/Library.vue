<template>
    <div>
        <Search @search="showResults" :books="books"/>
        <Books class="books" :books="result" />
    </div>
</template>
<script>
import Search from './Search.vue'
import Books from './Books.vue'
export default {
    name: 'Library',
    components: {
        Search,
        Books
    },
    data(){
        return {
            books: [
                {title: 'война и мир', author: 'Лев Николаевич Толстой'},
                {title: 'том Соер', author: 'Иван'},
                {title: 'преступление и наказание', author: 'Достоевский'},
                {title: 'преступление и наказание', author: 'Достоевский'},
            ],
            result: []
        }
    },
    methods: {
        showResults(item){
            this.result = item
        }
        
    }    
    
}
</script>
<style >
    .books{
        display: flex;
        flex-wrap: wrap;
        max-width: 500px;
    }
</style>
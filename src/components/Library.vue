<template>
    <div>
        <Search/>
        <Books :books="books" />
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
            ],
            result: [],
            searchString: ''
        }
    }
    
}
</script>
<style >
    
</style>
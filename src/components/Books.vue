<template>
    <div>
        <Book v-for= "(book, index) in books" :key="index" :book="book"/>
    </div>
</template>
<script>
import Book from './Book.vue'
export default {
    name: 'Books',
    props: {
        books: Array
    },
    components: {
        Book
    }

}
</script>
<style>
    
</style>
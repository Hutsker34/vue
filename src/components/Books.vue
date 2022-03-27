<template>
    <div>
        <div class="defolt" v-if="books.length == 0 ">ничего не найдено</div>
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
    .defolt{
        margin: 15px 0 0 5px;
    }
</style>
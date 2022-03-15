<template>
    <div>
        {{book.author}},
        {{book.title}}
    </div>
</template>
<script>
export default {
    name: "Book",
    props: {
        book: Object
    }
}
</script>
<style>
    
</style>
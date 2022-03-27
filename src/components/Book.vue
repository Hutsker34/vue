<template>
    <div class='frame' >
    <div class="overlay"></div>
       <div class="text"><strong>Автор:</strong>{{book.author}}</div>
       <div class="text"><strong>Название:</strong>{{book.title}}</div>
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
    .frame{
        position: relative;
        width: 150px;
        height: 250px;
        border: 2px solid black;
        margin-top: 15px; 
        margin-right: 10px;
        background: url("https://ynpress.com/wp-content/uploads/2016/11/tumblr_m3tjnnFWeo1qfgwwmo1_1280.jpg");
        color: #FFFACD;
        font-size: 12px;
        display: flex;
        flex-direction: column-reverse;
        padding: 0 5px 5px 5px;
        box-sizing: border-box;
    }
    .overlay {
			position: absolute;
			background: rgba(0,0,0,0.30);
			top: 0;
			left: 0;
			bottom: 0;
			right: 0;
		}
    .text{
        position: relative;
    }
</style>
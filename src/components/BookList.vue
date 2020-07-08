<template>
  <div>
    <h1>{{title}}</h1>
    <ul> 
      <book_item v-for="book in books" :book='book'></book_item>
    </ul>
  </div>
</template>

<script>
import BookItem from './BookItem';
export default {
  name: 'BookList',
  components:{
    BookItem

  },
  data() {
    return {
      title: 'All Books',
      books: [
        {title: 'Self-Reliance', author: 'Ralph Waldo Emerson'},
        {title: 'American Gods', author: 'Neil Gaiman'},
        {title: 'Amusing Ourselves to Death', author: 'Neil Postman'},
      ]
    };
  }
};
</script>

<style>
h1, h2 {
  font-weight: normal;
}

 ul{
  padding:0;
  list-style-type: none;

 }
 li{
 display: block;
 margin: 0 10px;

 }
</style> 
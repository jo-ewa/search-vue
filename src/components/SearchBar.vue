<template>
  <div class="search-bar">
    Search: <input type="text" v-model="bookTitle">
    <button @click="getBook()">Change Text</button>
    <!-- <div>
      <ol>
        <li v-for="book in bookResults" :key="book.id">
          <img :src="'https://books.google.com/books/content?id=' + book.id + '&printsec=frontcover&img=1&zoom=6&edge=curl&source=gbs_api'">
      
        </li>
      </ol>
    </div> -->
    {{bookResults}}
  </div>
</template>

<script>
export default {
  name: 'SearchBar',
  props: {
    propdata: String
  },
  
  data : function () {
    return {
      bookTitle:'',
      bookResults:[],
    }
  },

  // beforeMount(){
  //   this.getName();
  // },

  methods : {
    changeText : function () {
      console.log(this.datadata) 
    },
    async getBook(){
      const res = await fetch('https://www.googleapis.com/books/v1/volumes?q=' + this.bookTitle);
      const data = await res.json();
      this.bookResults = data;
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  input {border-radius: 5px; border: 1px solid gray;}
</style>

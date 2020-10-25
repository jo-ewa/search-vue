<template>
  <div class="search-bar">
    {{propdata}}
    Search: <input type="text" v-model="datadata">
    <button @click="changeText()">Change Text</button>
    {{datadata}}
    {{data}}
  </div>
</template>

<script>
export default {
  name: 'SearchBar',
  props: {
    propdata: String
  },
  
  data : function () {
    return{
      datadata:"Selfdata",
      data:{}
    }
  },

  beforeMount(){
    this.getName();
  },

  methods : {
    changeText : function () {
      console.log(this.datadata) 
    },
    async getName(){
      const res = await fetch('https://www.googleapis.com/books/v1/volumes?q=search-terms&key=AIzaSyChtwl0PwpT6itmLCovi6slyQL52Vt-wD0');
      const data = await res.json();
      this.data = data;
    }
    // async apiHandler : function () {
    //   const res = await fetch('https://www.googleapis.com/books/v1/volumes?q=search-terms&key=AIzaSyChtwl0PwpT6itmLCovi6slyQL52Vt-wD0');
    //   const data = await res.json();
    //   this.data = data;

    // }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  input {border-radius: 5px; border: 1px solid gray;}
</style>

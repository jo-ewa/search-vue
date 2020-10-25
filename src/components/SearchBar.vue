<template>
  <div class="search-bar">
    {{propdata}}
    Search: <input type="text" v-model="datadata">
    <button @click="ChangeText()">Change Text</button>
    {{datadata}}
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
      datadata:"Selfdata"
    }
  },

  methods : {
    ChangeText : function () {
      console.log(this.datadata) 
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  input {border-radius: 5px; border: 1px solid gray;}
</style>

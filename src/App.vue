<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <SearchBar propdata="Prop data"/>
  <ResultSet :resultList="searchResults"/>
</template>

<script>
import SearchBar from './components/SearchBar.vue'
import ResultSet from './components/ResultSet.vue'

export default {
  name: 'App',
  components: {
    SearchBar,
    ResultSet, 
  },
  data: function () {
    return {
      searchResults: [
        {title:"hello world" , desc: "first item on the list of results"},
        {title:"hola mundo" , desc: "second item on the list of results"},
      ]
    }
  },
  methods: {
    doSearch: function () {
      console.log("Search to be implemented")
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

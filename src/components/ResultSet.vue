<template>
  <div class="result-set">
    This is the result set
    <SingleResult v-for="result in resultList" v-bind:key="result" :title="result.title" :desc="result.desc"/>
  </div>
</template>

<script>

import SingleResult from './SingleResult.vue'

export default {
  name: 'ResultSet',
  props: {
      resultList: Array
  },

  components : {
      SingleResult
  },
  
  data : function () {
    return{

    }
  },

  methods : {
    countResults: function () {
      return this.resultList.length;  
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

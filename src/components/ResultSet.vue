<template>
  <div class="result-set">
    This is the result set
    <SingleResult/>
  </div>
</template>

<script>

import SingleResult from './SingleResult.vue'

export default {
  name: 'ResultSet',
  props: {
      msg: String
  },

  components : {
      SingleResult
  },
  
  data : function () {
    return{

    }
  },

  methods : {

  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

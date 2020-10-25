<template>
  <div class="single-result">
    <span class="title">{{title}}</span><br>
    <span class="desc">{{desc}}</span>
  </div>
</template>

<script>
export default {
  name: 'SingleResult',
  props: {
    title: String,
    desc: String,
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
  .title {font-size: 17px; color:blue}
  .desc  {font-size: 13px; color:green}
</style>

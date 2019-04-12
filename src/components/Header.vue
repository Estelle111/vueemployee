<template>
  <div class="headerCard">{{msg}}</div>
</template>

<script>
  export default {
    data() {
      return {
     
      }
    },
    props: {
        msg: String
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .headerCard {
    width: 440px;
    height: 45px;
    border: 1px solid blue;
  }
</style>

<template>
  <div class="EmployeeProfileCard">
    <Profile></Profile>
  </div>
</template>

<script>
  import Profile from './Profile.vue'

  export default {
    components: {
      Profile
    },
    data() {
      return {
     
      }
    },
    props: {
      profiles: Array
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .EmployeeProfileCard {
    width: 440px;
    height: 652px;
    border: 1px solid grey;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
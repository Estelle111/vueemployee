<template>
  <div class="EmployeePageCard">
    <Header :msg="msg1"></Header>
    <EmployeeProfile></EmployeeProfile>
  </div>
</template>

<script>
  import Header from './Header.vue'
  import EmployeeProfile from './EmployeeProfile.vue'
  
  export default {
    components: {
      Header,
      EmployeeProfile
    },
    data() {
      return {
        msg1: "Employee"
      }
    },
    props: {
      profiles: Array
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .EmployeePageCard {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    width: 450px;
    height: 710px;
    border: 1px solid brown;
  }
</style>
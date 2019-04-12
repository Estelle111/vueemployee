<template>
  <div class="HomePageCard">
    <Header :msg="msg2"></Header>  
    <SearchBar></SearchBar>
    <EmployeeList :profiles="profiles" :getInfo="getInfo"></EmployeeList>
  </div>
</template>

<script>
  import Header from './Header.vue';
  import SearchBar from './SearchBar.vue';
  import EmployeeList from './EmployeeList.vue';

  export default {
    components: {
      Header,
      SearchBar,
      EmployeeList
    },
    data() {
      return {
        msg2: "Employee Directory"
        }
    },
    props: {
      profiles: Array,
      appInfo: Function

    },
    methods: {
      getInfo(x) {
        this.appInfo(x)
      }
    }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .HomePageCard {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    width: 450px;
    height: 710px;
    border: 1px solid #ebeb32;
  }
</style>

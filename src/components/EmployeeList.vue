<template>
  <div class="EmployeeListCard" >
      <EmployeeListItem 
      :itemInfo="itemInfo"
      v-for='(profile, index) in profiles' 
      :key="index" 
      :profile="profiles[index]"></EmployeeListItem>
  </div>
</template>

<script>
  import EmployeeListItem from './EmployeeListItem'

  export default {
    components: {
      EmployeeListItem
    },
    props: {
      profiles: Array,
      getInfo: Function
    },
    methods: {
      itemInfo(obj) {
        this.getInfo(obj)
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .EmployeeListCard {
    width: 440px;
    height: 600px;
    border: 1px solid purple;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
}
</style>
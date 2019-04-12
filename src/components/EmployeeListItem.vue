<template>
  <div>
    <div class="EmployeeListItemCard" @click="handleClick">
      <div>
        <img :src="profile.photo" :alt="profile.name">
      </div>
      <div>
        <p>{{profile.name}}</p>
        <p>{{profile.job}}</p>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
        profile: Object,
        itemInfo: Function
    },
    methods: {
      handleClick(){
        let info = this.profile
        this.itemInfo(info) 
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .EmployeeListItemCard {
    width: 430px;
    height: 90px;
    border: 1px solid pink;
    margin-top: 5px;
    cursor: pointer;
    display: flex;
    justify-content: space-around;
    align-items: center;
  }
  img {
    width: 40px;
  }
</style>
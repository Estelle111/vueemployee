<template>
  <div id="app">
    <HomePage :profiles="profiles" :appInfo="appInfo"></HomePage>
    <EmployeePage></EmployeePage>
  </div>
</template>

<script>
import HomePage from './components/HomePage.vue'
import EmployeePage from './components/EmployeePage.vue'

export default {
  name: 'app',
  components: {
    HomePage,
    EmployeePage
  },
  data() {
    return {
      profiles: [
              {photo: 'assets/girl1.png', name: 'Sugar Barb', job: 'Cola Engineer'},
              {photo: 'assets/girl2.png', name: 'Greta Node', job: 'Data Designer'},
              {photo: 'assets/boy1.png', name: 'Jason Sass', job: 'Sparkle Manager'},
              {photo: 'assets/girl3.png', name: 'Sally Knee', job: 'Corpus Director'},
              {photo: 'assets/boy2.png', name: 'Maes Pills', job: 'Grizly Hunter'},
              {photo: 'assets/girl4.png', name: 'Rachel Bouglione', job: 'Circus Productor'},
          ],
      objectToDisplay: ''
    }
  },
  methods: {
    appInfo(y) {
      this.objectToDisplay = y
    }
  }

}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: auto;
  margin-top: 80px;
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 910px;
  height: 720px;
  border: 1px solid black;
}
</style>

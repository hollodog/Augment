<script>
import Vue from 'vue'
import axios from 'axios'
import Valorant from './components/Valorant.vue'

Vue.component('app', Valorant);

new Vue({
  el: '#app',
  data () {
    return {
      msg: 'Sample text'
    }
  },
  mounted () {
    axios
      .get('https://jsonplaceholder.typicode.com/posts')
      .then(response => (console.log(response.data)))
  },
  name: 'App',
  components: {
    Valorant
  }
})

export default Vue;
</script>

<template>
  <body>
    <div id="app">
      <Valorant msg="Welcome to Your Vue.js App"/>
    </div>
  </body>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

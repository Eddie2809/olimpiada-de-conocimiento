<script>
  import Home from './components/Home.vue'
  import Jugar from './components/Jugar.vue'

  export default{
    components: {
      Home,
      Jugar
    },
    data(){
      return{
        route: 0
      }
    },
    methods: {
      changeRoute(newRoute){
        this.route = newRoute
      }
    }
  }
</script>

<template>
  <div class="App">
    <Home v-if="route === 0" :changeRoute = "changeRoute"/>
    <Jugar v-if="route === 1"/>
  </div>
 </template>
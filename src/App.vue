<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <NewCompo v-bind:todos="todos"/>
    {{msg}}
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import NewCompo from './components/NewCompo.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    NewCompo
  },
  data(){
    return{
      todos:[
        {
          id:1,
          title:"todo one",
          completed:false
        },
        {
          id:2,
          title:"todo two",
          completed:true
        },
        {
          id:3,
          title:"todo three",
          completed:true
        }
      ]
    }
  }
}
</script>

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

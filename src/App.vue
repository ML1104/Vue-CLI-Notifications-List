<template>
  <div id="app">
    <HelloWorld msg="Notifications List"/>
    <Notifications/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Notifications from './components/Notifications.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Notifications
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  border: 1px solid black;
}
</style>

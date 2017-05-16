<template>
  <div id="app">
    <navbar></navbar>
    <task></task>
    <formulaire></formulaire>
    <router-view></router-view>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar'
import Task from '@/components/Task'
import AddTask from '@/components/AddTask'
export default {
  name: 'app',
  components: {navbar: Navbar, task:Task, formulaire: AddTask}
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>

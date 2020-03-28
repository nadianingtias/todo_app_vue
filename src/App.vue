<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <ProjectPage />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import ProjectPage from './components/ProjectPage.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    ProjectPage
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
.bd-example {
        padding: 1.5rem;
        margin-right: 0;
        margin-left: 0;
        border-width: .2rem;
        border: solid #f7f7f9;
    }
</style>

<template>
  <Header/>
  <NavBar/>
  <Projects />
</template>

<script>
import Header from './components/Header.vue';
import NavBar from './components/NavBar.vue';
import Projects from './components/Projects.vue';

export default {
  name: 'App',
  components: {
    Header,
    NavBar,
    Projects
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
}
body {
  margin: 0;
}
</style>

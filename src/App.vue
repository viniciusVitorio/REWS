<template>
  <Header/>
  <NavBar/>
  <Projects />
  <br>
  <Map />
  <br>
  <EmergencyNumbers />
  <br>
  <Services />
</template>

<script>
import Header from './components/Header.vue';
import NavBar from './components/NavBar.vue';
import Projects from './components/Projects.vue';
import Map from './components/Map.vue';
import EmergencyNumbers from './components/EmergencyNumbers.vue';
import Services from './components/Services.vue';

export default {
  name: 'App',
  components: {
    Header,
    NavBar,
    Projects,
    Map,
    EmergencyNumbers,
    Services
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

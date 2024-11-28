<template>
    <section class="text-center">
      <Title title="MAPA DE ABRIGOS" />
      <div class="map-container mt-4">
        <iframe 
          src="https://www.google.com/maps/d/embed?mid=1BFoe-q2LJHLd66R0MpianejE30_XYkdo&ehbc=2E312F" 
          width="100%" 
          height="100%" 
          allowfullscreen="" 
          loading="lazy">
        </iframe>
      </div>
    </section>
  </template>
  
  <script>
  import Title from "./Title.vue";
  
  export default {
    name: "Map",
    components: {
      Title,
    },
  };
  </script>
  
  <style scoped>
  .map-container {
    position: relative;
    width: 100%;
    padding-top: 56.25%; /* Aspect Ratio de 16:9 */
    overflow: hidden;
  }
  
  .map-container iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 0;
  }
  </style>
  
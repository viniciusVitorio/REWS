<template>
    <div>
        <Title title="CONTATOS EMERGENCIAIS" />
        <section class="emergency-numbers text-center">
        <ul class="numbers-list">
            <li v-for="number in emergencyNumbers" :key="number.name">
            <strong>{{ number.name }}:</strong> <a :href="`tel:${number.phone}`">{{ number.phone }}</a>
            </li>
        </ul>
        </section>
    </div>
  </template>
  
  <script>
  import Title from "./Title.vue";

  export default {
    name: "EmergencyNumbers",
    components: {
      Title,
    },
    data() {
      return {
        emergencyNumbers: [
          { name: "Defesa Civil", phone: "199" },
          { name: "Polícia Militar", phone: "190" },
          { name: "Bombeiros", phone: "193" },
          { name: "SAMU (Emergência Médica)", phone: "192" },
          { name: "Disque Denúncia", phone: "181" },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .emergency-numbers {
    margin: 20px auto;
    padding: 20px;
    max-width: 400px;
    background-color: #f8f9fa;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }
  
  .title {
    font-size: 1.5rem;
    color: #333;
    margin-bottom: 1rem;
  }
  
  .numbers-list {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  
  .numbers-list li {
    margin: 10px 0;
    font-size: 1rem;
    color: #555;
  }
  
  .numbers-list a {
    color: #007bff;
    text-decoration: none;
  }
  
  .numbers-list a:hover {
    text-decoration: underline;
  }
  </style>
  
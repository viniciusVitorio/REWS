<template>
    <div>
        <Title title="SERVIÇOS" />
        <section class="services text-center">
      <ul class="services-list">
        <li v-for="service in services" :key="service.name">
          <a :href="service.link" target="_blank" rel="noopener noreferrer">
            {{ service.name }}
          </a>
        </li>
      </ul>
    </section>
    </div>
  </template>
  
  <script>
  import Title from "./Title.vue";

  export default {
    name: "Services",
    components: {
      Title,
    },  
    data() {
      return {
        services: [
          {
            name: "Denúncias Ambientais",
            link: "https://riodosul.atende.net/autoatendimento/servicos/denuncias-ambientais",
          },
          {
            name: "Licenças Ambientais",
            link: "https://riodosul.atende.net/autoatendimento/servicos/licencas-ambientais-em-analise",
          },
          {
            name: "Demais Serviços",
            link: "https://riodosul.atende.net/autoatendimento",
          },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
.services {
  margin: 20px auto;
  padding: 20px;
  max-width: 500px;
  background-color: #f8f9fa;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.title {
  font-size: 1.5rem;
  color: #333;
  margin-bottom: 1rem;
}

.services-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.services-list li {
  margin: 10px 0;
}

.services-list a {
  display: inline-block;
  padding: 12px 25px;
  font-size: 1.1rem;
  font-weight: 500;
  color: #fff;
  text-align: center;
  text-decoration: none;
  background-color: #007bff;
  border-radius: 5px;
  transition: background-color 0.3s ease, transform 0.2s ease;
}

.services-list a:hover {
  background-color: #0056b3;
  transform: scale(1.05);
}
</style>

  
<template>
  <section class="text-center">
    <Title title="PROJETOS" />
    <div class="mt-4">
        <img :src="imageSrc" alt="Imagem do projeto" class="w-full max-w-md rounded-lg shadow-lg mx-auto" />
    </div>
  </section>
</template>

<script>
import Title from "./Title.vue";
import imageSrc from "../assets/images/Riodosul1.jpg";

export default {
  name: 'Projects',
  components: {  
    Title
  },
  data() {
    return {
      imageSrc
    };
  }
}
</script>
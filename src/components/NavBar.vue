<template>
    <nav class="flex justify-between items-center p-5">
        <div class="flex space-x-2 items-center">
            <button @click="toggleMenu" class="focus:outline-none">
                <PhList :size="28" />
            </button>
            <PhUser :size="28" />
        </div>
    
        <div class="flex items-center bg-teal-800 text-white rounded-full px-4 py-2 max-w-md mx-auto">
            <PhMagnifyingGlass class="mr-2" size="20" />
            <input
              type="text"
              placeholder="Pesquisar"
              class="bg-transparent outline-none placeholder-white text-white w-full"
            />
        </div>
        <HamburgerMenu :isOpen="menuOpen" @close="menuOpen = false" />
    </nav>
</template>

<script>
import { PhUser, PhList, PhMagnifyingGlass } from "@phosphor-icons/vue";
import HamburgerMenu from "./HamburgerMenu.vue";

export default {
  name: 'NavBar',
  components: {
    PhUser,
    PhList,
    PhMagnifyingGlass,
    HamburgerMenu
  },
  data() {
    return {
      menuOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen;
    }
  }
}
</script>

<style scoped>
</style>

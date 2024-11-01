<template>
  <div v-show="isOpen" class="fixed inset-0 bg-black bg-opacity-50 flex z-50" @click.self="closeMenu">
    <div 
      v-show="isOpen"
      class="bg-white w-64 p-4 h-full shadow-lg"
      :class="{ 'translate-x-0': isOpen }"
    >
      <button @click="closeMenu" class="text-gray-500 mb-4">Fechar</button>
      <ul>
        <li class="p-2 hover:bg-gray-100 cursor-pointer">Exemplos</li>
        <li class="p-2 hover:bg-gray-100 cursor-pointer">Educação</li>
        <li class="p-2 hover:bg-gray-100 cursor-pointer">Serviços</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HamburgerMenu',
  props: {
    isOpen: {
      type: Boolean,
      required: true
    }
  },
  methods: {
    closeMenu() {
      this.$emit('close');
    }
  }
}
</script>
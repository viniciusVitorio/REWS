<template>
  <div class="text-center">
    <h3 class="text-3xl font-bold tracking-wide">{{ title }}</h3>
  </div>
</template>

<script>
export default {
  name: 'TitleComponent',
  props: {
    title: {
      type: String,
      required: true
    }
  }
}
</script>

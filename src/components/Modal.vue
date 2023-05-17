<template>
  <div class="backdrop" @click="closeModal">
    <div class="modal" :class="{ sale: theme === 'sale' }">
      <h1>{{ header }}</h1>
      <p>{{ content }}</p>
      <button @click="toggleModal">Close Modal</button>
    </div>
  </div>
</template>

<script>
export default {
  props: ['header', 'content', 'theme'],
  methods: {
    closeModal() {
      this.$emit('close')
    }
  }
}
</script>


<template>
  <div class="container">
    <h1>{{ title }}</h1>
    <div v-if="showModal">
      <Modal theme="sale">
        <h1>{{ header }}</h1>
        <p>{{ content }}</p>
        <button @click="toggleModal">Close Modal</button>
      </Modal>
    </div>
    <button @click="toggleModal">Open Modal</button>
  </div>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: { Modal },
  data() {
    return {
      title: 'My Journey of love',
      header: 'Add account for love',
      content: 'Love is patience',
      showModal: false
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
    }
  }
}
</script>


<style>
</style>
<template>
  <div id="app">
    <button class="btn btn-primary btn-dark modal-btn" @click="toggleModal">Open Modal</button>
    <counter />
    
    <Modal :modalActive="modalActive" @close-modal="toggleModal"> 
      <h1>Counter App</h1>
      <p>
        The counter is a simple application built with Vue.js, designed to increment or decrement a value with button clicks. 
        The counter value is saved in the browser's local storage. This application was created to practice Vue.js development.</p>
    </Modal>
  </div>
</template>

<script>
import { ref } from 'vue';
import counter from './components/counter.vue'
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: {
    counter,
    Modal
  },
  setup() {
    const modalActive = ref(false);
    const toggleModal = () => {
      modalActive.value = !modalActive.value;
    }

    return {
      modalActive,
      toggleModal
    };
  }
}
</script>

<style>
#app {
  font-family: "Anton SC", sans-serif;
  font-weight: 400;
}

.modal-btn {
  margin: 2rem;
  position: absolute;
  top: 0;
  left: 0;
}
</style>

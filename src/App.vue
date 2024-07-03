<template>
  <div id="app">
    <counter></counter>
  </div>
</template>

<script>
import counter from './components/counter.vue'

export default {
  name: 'App',
  components: {
    counter
  }
}
</script>

<style>
#app {
  font-family: "Anton SC", sans-serif;
  font-weight: 400;
}
</style>

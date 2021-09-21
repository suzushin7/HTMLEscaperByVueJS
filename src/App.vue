<template>
  <div id="app">
    <HTMLEscaper />
  </div>
</template>

<script>
import HTMLEscaper from './components/HTMLEscaper.vue'

export default {
  name: 'HTML Escaper',
  components: {
    HTMLEscaper
  }
}
</script>

<style>
#app {
  font-size: 15px;
}
</style>

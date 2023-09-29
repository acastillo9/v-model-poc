<template>
  <div id="app">
    <p>{{ checked }}</p>
    <FieldWrapper v-model="checked" />
  </div>
</template>

<script>
import FieldWrapper from './components/FieldWrapper.vue';

export default {
  name: 'App',
  components: {
    FieldWrapper,
  },
  data() {
    return {
      checked: false,
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

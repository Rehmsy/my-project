<template>
  <div id="app">
    <Cats
      v-bind:cats="cats"
      v-bind:selected="selected"
      v-bind:onSelect="handleSelect"/>
    <Playa
      v-bind:cat="selected"/>
  </div>
</template>

<script>
import Cats from './components/Cats';
import Playa from './components/Playa';
import cats from './cat-data.js';

export default {
  data() {
    return {
      cats,
      selected: null
    };
  },
  components: {
    Cats,
    Playa
  },
  methods: {
    handleSelect(cat) {
      this.selected = cat;
    }
  }
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

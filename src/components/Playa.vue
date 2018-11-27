<template>
  <section class="kitties">
    <div v-if="cat">
      <h2>{{cat.name}}</h2>
      <h3>I {{cat.quality}}</h3>
      <img v-bind:src="cat.image">
    </div>
    <div class="else" v-else>Pick a kitty</div>
  </section>
</template>

<script>
export default {
  props: {
    cat: Object
  }
};
</script>

<style>

h2 {
  margin-top: 50px;
  margin-bottom: 40px;
}
img {
  padding: 10px;
  height: 200px;
}
.else {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  font-size: 4em;
  color: #2c3e50;
  margin-top: 60px;
}

</style>

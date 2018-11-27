<template>
  <section>
    <div v-if="cat">
      <h2>{{cat.name}}</h2>
      <p>{{cat.quality}}</p>
      <img v-bind:src="cat.image">
    </div>
    <div v-else>Pick a kitty</div>
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

</style>

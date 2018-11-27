<template>
  <ul class="cats">
    <li v-for="cat in cats"
      v-bind:class="{ cat: true, selected: cat === selected }"
      v-bind:key="cat.name"
      v-on:click="onSelect(cat)">
      <img v-bind:src="cat.image">
      <h2>{{cat.name}} the {{cat.quality}}</h2>
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    cats: Array,
    selected: Object,
    onSelect: Function
  }
};
</script>

<style>

.cats {
  display: flex;
  flex-wrap:wrap;
}

.cat {
  list-style: none;
  position: relative;
  height: 250px;
  width: 250px;
  border: 2px solid pink;
}

.cat.selected {
  background: lightsteelblue;
}

</style>

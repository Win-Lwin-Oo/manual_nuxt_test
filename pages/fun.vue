<template>
  <div>
    <h1 class="red">Hello {{ name }}!</h1>
    <LazyMountainsList v-if="show" />
    <button v-if="!show" @click="showList()">Show List</button>
  </div>
</template>

<script>
export default {
  // page properties go here
  data() {
    return {
        name: 'test',
        show: false,
    };
  },
  methods: {
    showList() {
      this.show = true;
    },
  },
};
</script>

<style>
.red {
  color: red;
}
</style>
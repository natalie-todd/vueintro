<template>
  <div id="app">
    <h1>{{msg}}</h1>
    <p v-if="isAwesome">Galvanize is awesome</p>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      msg: 'Hello Galvanize',
      isAwesome: true,
    };
  },
};
</script>

<style>

</style>

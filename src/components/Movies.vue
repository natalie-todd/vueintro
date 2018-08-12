<template lang="html">
    <div>
        <h1>Movies!</h1>
        <form @submit.prevent="searchForMovies()">
            <label for="search">Search</label>
            <input v-model="searchTerm" type="text" name="search" id="search" value="">
            <button type="submit" name="button">Search for Movies!</button>
        </form>
        <h3>{{searchTerm}}</h3>
        </div>
</template>

<script>
export default {
  data() {
    return {
      searchTerm: ""
    };
  },
  methods: {
    searchForMovies() {
      console.log("Searching for movies.");
    }
  }
};
</script>

<style lang="css">
</style>
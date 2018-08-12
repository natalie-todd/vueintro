<template lang='html'>
    <div>
        <h1>Movies!</h1>
        <form @submit.prevent='searchForMovies()'>
            <label for='search'>Search</label>
            <input v-model='searchTerm' type='text' name='search' id='search' value=''>
            <button type='submit' name='button'>Search for Movies!</button>
        </form>
        <ul>
            <li v-for='movie in movies'>{{movie.Title}}</li>
        </ul>
        </div>
</template>

<script>
export default {
  data() {
    return {
      searchTerm: '',
      movies: [],
    };
  },
  methods: {
    searchForMovies() {
      const API_URL = `https://omdb-api.now.sh/?s=${this.searchTerm}`;
      //   fetch();
      fetch(API_URL)
      .then(res => res.json())
      .then(result => {
          this.movies = result.Search;
      })
    },
  },
};
</script>

<style lang='css'>
</style>
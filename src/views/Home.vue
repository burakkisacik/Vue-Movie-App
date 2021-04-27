<template>
  <div class="home">
    <SearchBox @gotMovies="moviesArrayHandler" />
    <MovieList :movielist="movies" />
  </div>
</template>

<script>
import SearchBox from '../components/SearchBox';
import MovieList from '../components/MovieList';
export default {
  name: 'Home',
  components: {
    SearchBox,
    MovieList,
  },
  data() {
    return {
      movies: [],
    };
  },
  methods: {
    moviesArrayHandler: function(movieArray) {
      this.movies = movieArray;
    },
  },
};
</script>

<style>
.home {
  max-width: 600px;
  height: 100vh;
  margin: 0 auto;
}
</style>

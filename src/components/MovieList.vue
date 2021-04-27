<template>
  <div
    class="movieList-container"
    v-for="movie in movielist"
    :key="movie.imdbID"
  >
    <Movie :title="movie.Title" :year="movie.Year" :poster="movie.Poster" />
  </div>
</template>

<script>
import Movie from './Movie';
export default {
  name: 'MovieList',
  components: {
    Movie,
  },
  props: ['movielist'],
};
</script>

<style></style>

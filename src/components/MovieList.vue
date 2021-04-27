<template>
  <div class="movieList-container">
    <Movie />
    <Movie />
    <Movie />
    <Movie />
    <Movie />
  </div>
</template>

<script>
import Movie from './Movie';
export default {
  name: 'MovieList',
  components: {
    Movie,
  },
};
</script>

<style></style>

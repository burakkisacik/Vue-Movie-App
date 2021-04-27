<template>
  <div class="home">
    <SearchBox />
    <MovieList />
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
  setup() {},
};
</script>

<style>
.home {
  max-width: 600px;
  height: 100vh;
  margin: 0 auto;
}
</style>

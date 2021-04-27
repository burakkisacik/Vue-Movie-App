<template>
  <div class="search-box">
    <input
      @keyup.enter="fetchMovie"
      class="search-bar"
      type="text"
      placeholder="Search..."
      v-model="searchMovie"
    />
  </div>
</template>

<script>
export default {
  name: 'SearchBox',
  data() {
    return {
      searchMovie: '',
      foundedMovies: [],
    };
  },
  methods: {
    fetchMovie: async function() {
      const res = await fetch(
        `http://www.omdbapi.com/?apikey=995242b5&s=${this.searchMovie}&type=movie`
      );
      const data = await res.json();
      this.foundedMovies = data.Search;
      this.searchMovie = '';
      this.$emit('gotMovies', this.foundedMovies);
    },
  },
};
</script>

<style>
.search-box {
  width: 100%;
  margin-top: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.search-bar {
  display: block;
  padding: 15px;
  width: 90%;
  color: #313131;
  font-size: 20px;
  appearance: none;
  border: none;
  outline: none;
  background: none;
  box-shadow: 0 0 8px rgba(0, 0, 0, 0.25);
  background-color: white;
  /* background-color: rgba(255, 255, 255, 0.5); */
  border-radius: 0 16px 0 16px;
  transition: 0.4s;
}

.search-bar:focus {
  background-color: rgba(255, 255, 255, 0.75);
  box-shadow: 0 0 16px rgba(0, 0, 0, 0.25);
  border-radius: 16px 0 16px 0;
}
</style>

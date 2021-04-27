<template>
  <div class="container">
    <div class="img-filter">
      <h1 class="title">The X Files</h1>
      <h2 class="year">Year : 1994</h2>
      <p class="desc">
        Decrition Lorem ipsum dolor sit amet, consectetur adipisicing elit.
        Possimus voluptatum veritatis accusantium cupiditate optio vero.
      </p>
    </div>

    <img
      class="poster"
      src="https://m.media-amazon.com/images/M/MV5BMmY4MjgxNjUtZTY2Mi00YzdiLTk3ZjctZmY5NTA4YzUwMjNiXkEyXkFqcGdeQXVyMzM4MjM0Nzg@._V1_SX300.jpg"
      alt=""
    />
  </div>
</template>

<script>
export default {
  name: 'Movie',
};
</script>

<style scoped>
.container {
  display: inline-block;
  overflow: hidden;
  position: relative;
  margin-top: 20px;
  width: 100%;
  height: 400px;
  color: white;
  border-radius: 20px;
}

.poster {
  pointer-events: none;
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: -1;
}

.img-filter {
  position: absolute;
  padding: 10px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;

  bottom: 0;
  left: 0;
  width: 100%;
  height: 200px;
  background: linear-gradient(
    180deg,
    rgba(255, 255, 255, 0),
    rgba(0, 0, 0, 0.8) 10%
  );
  font-weight: bold;
  z-index: 0;
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
}
</style>

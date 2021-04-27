<template>
  <div class="search-box">
    <input class="search-bar" type="text" placeholder="Search..." />
  </div>
</template>

<script>
export default {
  name: 'SearchBox',
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

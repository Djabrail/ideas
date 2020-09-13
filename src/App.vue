<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;800&display=swap");
body {
  font-family: "Montserrat", Open Sans, system-ui, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c2c2c;
  background-color: #f6f7f8;
}
.container {
  width: 640px;
  margin: 50px auto;
}
* {
  border: 0;
  outline: none;
  list-style: none;
  padding: 0;
  margin: 0;
}
</style>

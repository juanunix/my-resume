<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>

html, body {
  font-family: 'Roboto', sans-serif;
  width: 100%;
  height: 100%;
  margin: 0;
}

#app {
  height: 100%;
}

</style>

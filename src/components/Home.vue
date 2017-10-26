<template>
  <div class="wrapper">
    <section></section>
    <main></main>
  </div>
</template>

<script>
  export default {
    name: 'Home'
  }
</script>

<style lang='scss' scoped>

@import '../App.scss';

.wrapper {
  width: 100%;
  height: 100%;
  display: grid;
  grid-template-rows: 30px [main] 1fr 30px;
  grid-template-columns: 10% [profile] minmax(auto, 300px) [main] 2fr 10%;
  grid-gap: 10px;
}
  
section {
  grid-row: main;
  grid-column: profile;
  background-color: $main-color;
}

main {
  grid-row: main;
  grid-column: main;
  background-color: $gray-color;
}

@include media-breakpoint-tablet {

  .wrapper {
    grid-template-columns: 5% [profile] 1fr [main] 2fr 5%;
  }
}

@include media-breakpoint-mobile {
  
  .wrapper {
    grid-template-rows: 1% [profile] 1fr [main] 2fr 1%;
    grid-template-columns: 1% [main] 1fr 1%;
  }

  section {
    grid-row: profile;
    grid-column: main;
  }

  main {
    grid-row: main;
    grid-column: main;
  }
}

</style>
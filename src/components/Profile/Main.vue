<template>
  <section>
    <figure>
      <img src="./assets/profile-pic.jpg" alt="Profile picture">
    </figure>
  </section>
</template>

<script>
  export default {
    name: 'Profile'
  }
</script>

<style lang='scss' scoped>

@import '../../App.scss';

section {

  display: grid;
  grid-template-rows: [picture] 30% 70%;

  background-color: $main-color;

  figure {

    grid-row: picture;
    display: flex;
    align-items: center;
    justify-content: center;

    img {
      width: 200px;
      height: 200px;
      border-radius: 50%;
    }
  }
}

@include media-breakpoint-mobile {

  section {
    grid-template-rows: [picture] 60% 40%;
  }
}

</style>
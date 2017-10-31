<template>
  <section id="profile">
    <figure>
      <img src="./assets/profile-pic.jpg" alt="Profile picture">
    </figure>

    <section id="description">
      <h1 id="name">Gabriel Nuñez</h1>
      <span id="occupation">Frontend developer</span>
      <p>I'm always looking to keep up with the latest technological trends, and I'm committed to meet the specified goals and objectives.</p>
    </section>

  </section>
</template>

<script>
  export default {
    name: 'Profile'
  }
</script>

<style lang='scss' scoped>

@import '../../App.scss';

#profile {

  display: grid;
  grid-template-rows: [picture] 30% [description] 70%;

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

#description {

  grid-row: description;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 0 10%;

  #name {
    font-size: 25px;
    font-weight: bold;
  }

  #occupation {
    font-size: 18px;
  }

  p {
    text-align: justify;
  }
}

@include media-breakpoint-mobile {

  #profile {
    grid-template-rows: [picture] 40% [description] 60%;
  }
}

</style>
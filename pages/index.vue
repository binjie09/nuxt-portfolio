<template>
  <div id="main-wrapper">
    <Banner />
    <Projects></Projects>
    <Socials />
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Banner from '~/components/Banner.vue'
import Projects from '~/components/Projects.vue'
import Socials from '~/components/Socials.vue'

export default {
  components: {
    Logo,
    Banner,
    Projects,
    Socials
  }
}
</script>

<style lang="scss">
#main-wrapper {
  .main-btn {
    cursor: pointer;
    padding: 20px 40px;
    font-size: 1.5rem;
    background-color: rgba(0, 0, 0, 0);
    color: rgb(53, 73, 94);
    border: 1px solid rgb(53, 73, 94);
    transition: all .2s ease-out;

    &:hover {
      background-color: rgb(53, 73, 94);
      color: white;
    }
  }

  .full-height {
    height: 100vh;
    padding: 100px 0px;
  }

  .section-header {
    margin-bottom: 50px;

    .section-title {
      position: relative;
      font-size: 3em;
      font-weight: 300;
      color: rgb(82, 100, 136);
      display: initial;

      &::after {
        content: '';
        position: absolute;
        bottom: 35%;
        right: -120%;
        background-color: rgb(82, 100, 136);
        width: 100%;
        height: 1px;
      }
    }
  }
}
</style>

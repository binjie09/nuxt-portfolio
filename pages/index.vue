<template>
  <div id="main-wrapper">
    <Banner />
    <Socials />
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import Banner from '~/components/Banner.vue'
import Socials from '~/components/Socials.vue'

export default {
  components: {
    Logo,
    Banner,
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
}
</style>

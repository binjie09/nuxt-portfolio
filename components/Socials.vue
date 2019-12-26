<template>
  <div id="socials">
    <ul id="social-list">
      <li><i class="fab fa-github"></i></li>
      <li><i class="fab fa-linkedin-in"></i></li>
      <li><i class="far fa-envelope"></i></li>
      <li><i class="fab fa-stack-overflow"></i></li>
    </ul>
  </div>
</template>

<style scoped lang="scss">
#socials {
  position: fixed;
  right: 5%;
  bottom: 0;

  #social-list {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;

    li {
      margin-bottom: 5px;

      i {
        font-size: 1.4rem;
      }
    }


    &::after {
      content: '';
      display: inline-block;
      width: 1px;
      height: 75px;
      margin-top: 15px;
      background-color: rgb(53, 73, 94);
    }
  }
}
</style>

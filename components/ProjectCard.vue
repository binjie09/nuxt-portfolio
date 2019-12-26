<template>
  <div class="project-card">
    <img :src="project.img_url" alt="">
    <div class="card-content">
      <div class="card-text">
        <a href="#"><i class="fab fa-github gh-link"></i></a>
        <h1 class="project-title">{{ project.title }}</h1>
        <p class="project-desc">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Error dicta enim officiis saepe tenetur fugiat commodi vitae asperiores. Animi eius iste dolorem, nisi porro rem nihil numquam facilis deserunt perspiciatis.</p>
        <div class="project-links">
          <a href="#"><i class="fas fa-eye"></i></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: [ 'project' ]
  }
</script>

<style scoped lang="scss">
  .project-card {
    width: 100%;
    height: 70%;
    display: flex;
    align-items: center;

    img {
      width: 60%;
      height: 100%;
      object-fit: cover;
    }

    .card-content {
      height: 100%;
      width: 100%;
      position: relative;

      .card-text {
        position: absolute;
        width: 135%;
        top: 45%;
        left: -35%;
        padding: 20px 30px;
        border-radius: 4px;
        box-shadow: 2px 0px 20px 4px rgba(0,0,0,0.15);
        background-color: rgb(82, 100, 136);
        color: white;
        text-align: justify;
        overflow: hidden;

        .project-title {
          font-size: 2em;
          font-weight: 300;
        }

        .gh-link {
          position: absolute;
          background-color: white;
          top: -50px;
          right: -60px;
          width: 120px;
          height: 100px;
          padding: 5px;
          display: flex;
          align-items: flex-end;
          justify-content: center;
          transform: rotate(0.125turn);
          font-weight: 300;
          font-size: 2rem;
        }

        .project-links {
          font-weight: 300;
          font-size: 3rem;

          a {
            color: white;
            text-decoration: none;

            &:hover {
              text-decoration: none;
            }
          }
        }
      }
    }
  }
</style>

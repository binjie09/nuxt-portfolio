<template>
  <div id="projects" class="full-height">
    <div class="container">
      <div class="section-header">
        <h1 class="title section-title">Projects</h1>
      </div>
      <div class="project-selector">
        <div v-for="(project, index) in projects"
             v-bind:class="{ active: selection === index }"
             class="project-btn"
             @click="selection = index">
             {{ project.title }}
        </div>
      </div>
      <ProjectCard :project="projects[selection]" />
    </div>
  </div>
</template>

<script>
  import data from '~/data.js'
  import ProjectCard from '~/components/ProjectCard.vue'

  export default {
    data () {
      return {
        selection: 0,
        projects: data
      }
    },
    components: {
      ProjectCard
    }
  }
</script>

<style scoped lang="scss">
  .container {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;

    .project-selector {
      display: flex;

      .project-btn {
        cursor: pointer;
        padding: 10px 20px;
        height: 40px;
        font-weight: 400;
        display: flex;
        align-items: center;
        justify-content: center;
        background-color: rgb(82, 100, 136);
        color: white;
      }

      .active {
        background-color: white;
        color: rgb(82, 100, 136);
      }
    }
  }
</style>

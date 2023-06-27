<template>
  <section id="projects" class="container mt-5">
    <div class="row">
      <div class="col">
        <h1 class="display-4">Projects</h1>
        <div v-for="project in projects" :key="project.id" class="card mt-3">
          <div class="card-body">
            <h5 class="card-title">{{ project.title }}</h5>
            <p class="card-text">{{ project.description }}</p>
            <a :href="project.link" class="btn btn-primary" target="_blank">View Project</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ProjectsSection',
  data() {
    return {
      projects: [
        {
          id: 1,
          title: 'Project 1',
          description: 'This is a description of Project 1',
          link: '#'
        },
        {
          id: 2,
          title: 'Project 2',
          description: 'This is a description of Project 2',
          link: '#'
        }
      ]
    }
  }
}
</script>

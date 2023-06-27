<template>
  <section id="skills" class="container mt-5">
    <div class="row">
      <div class="col">
        <h1 class="display-4">Skills</h1>
        <ul class="list-group mt-3">
          <li v-for="skill in skills" :key="skill" class="list-group-item">{{ skill }}</li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SkillsSection',
  data() {
    return {
      skills: ['JavaScript', 'Vue.js', 'React', 'Node.js']
    }
  }
}
</script>

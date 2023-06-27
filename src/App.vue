<template>
  <div id="app">
    <nav>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#skills">Skills</a>
      <a href="#contact">Contact</a>
    </nav>
    <About />
    <Projects />
    <Skills />
    <Contact />
  </div>
</template>

<script>
import About from './components/About.vue'
import Projects from './components/Projects.vue'
import Skills from './components/Skills.vue'
import Contact from './components/Contact.vue'

export default {
  mounted() {
    const links = document.querySelectorAll('nav a')
    links.forEach(link => {
      link.addEventListener('click', (e) => {
        e.preventDefault()
        const target = document.querySelector(e.target.getAttribute('href'))
        target.scrollIntoView({ behavior: 'smooth' })
      })
    })
  },
  name: 'App',
  components: {
    About,
    Projects,
    Skills,
    Contact
  }
}
</script>

<style>
/* Your styles here */
</style>

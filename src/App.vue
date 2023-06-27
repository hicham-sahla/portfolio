<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg fixed-top py-3 mb-3" :class="{ 'bg-primary': isScrolled }">
      <div class="container d-flex justify-content-between">
        <a class="navbar-brand" :class="{ 'text-white': isScrolled }" href="#" @click="redirectToLinkedIn">Hicham
          Sahla</a>
        <div class="collapse navbar-collapse justify-content-center">
          <ul class="navbar-nav mr-auto">
            <li class="nav-item">
              <a class="nav-link" :class="{ 'text-white': isScrolled }" href="#about">About</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" :class="{ 'text-white': isScrolled }" href="#projects">Projects</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" :class="{ 'text-white': isScrolled }" href="#skills">Skills</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" :class="{ 'text-white': isScrolled }" href="#contact">Contact</a>
            </li>
          </ul>
        </div>
        <button class="btn" :class="{ 'btn-primary': !isScrolled, 'btn-light': isScrolled }">CV</button>
      </div>
    </nav>
    <PageheaderSection />
    <AboutSection />
    <CareerSection />
    <ProjectsSection />
    <SkillsSection />
    <ContactSection />
  </div>
</template>

<script>
import AboutSection from './components/About.vue'
import CareerSection from './components/Career.vue'
import ProjectsSection from './components/Projects.vue'
import SkillsSection from './components/Skills.vue'
import ContactSection from './components/Contact.vue'
import PageheaderSection from './components/Pageheader.vue'

export default {
  name: 'App',
  data() {
    return {
      isScrolled: false,
    };
  },
  components: {
    AboutSection,
    CareerSection,
    ProjectsSection,
    SkillsSection,
    ContactSection,
    PageheaderSection
  },
  mounted() {
    const links = document.querySelectorAll('nav a')
    links.forEach(link => {
      link.addEventListener('click', (e) => {
        e.preventDefault()
        const target = document.querySelector(e.target.getAttribute('href'))
        target.scrollIntoView({ behavior: 'smooth' })
      })
    });
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.isScrolled = window.scrollY > 0;
    },
    redirectToLinkedIn(event) {
      event.preventDefault(); // prevent the default action
      window.open('https://www.linkedin.com/in/hicham-sahla/', '_blank');
    },
  },
}
</script>

<style>
/* Your styles here */
</style>

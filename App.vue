<template>
  <div id="app">
    <header class="site-header">
      <div class="container header__inner">
        <a href="#" class="brand" aria-label="Home">
          <span class="brand__logo">MD</span>
          <span class="brand__text">MBOUMANOU NGALEU MICHELLE</span>
        </a>
        <nav class="nav" aria-label="Primary">
          <ul class="nav__list">
            <li><a href="#about">About</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#experience">Experience</a></li>
            <li><a href="#case-studies">Case studies</a></li>
            <li><a href="#blog">Blog</a></li>
            <li><a href="#testimonials">Testimonials</a></li>
            <li><a href="#contact" class="btn btn--primary">Contact</a></li>
          </ul>
        </nav>
      </div>
    </header>

    <main>
      <Hero />
      <About />
      <Skills />
      <Projects :items="projects" />
      <Experience />
      <CaseStudies />
      <Blog />
      <Testimonials />
      <Contact />
    </main>

    <footer class="site-footer">
      <div class="container footer__inner">
        <div class="footer__brand">
          <span class="brand__logo">MD</span>
          <span class="brand__text">Michelle Destiny</span>
        </div>
        <div class="footer__links">
          <a href="#about">About</a>
          <a href="#projects">Projects</a>
          <a href="#blog">Blog</a>
          <a href="#contact">Contact</a>
        </div>
        <div class="footer__meta">
          <span>&copy; 2025</span>
          <a href="/assets/Michelle-Destiny-CV.pdf" target="_blank" rel="noopener">CV (PDF)</a>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import Skills from './components/Skills.vue'
import Projects from './components/Projects.vue'
import Experience from './components/Experience.vue'
import CaseStudies from './components/CaseStudies.vue'
import Blog from './components/Blog.vue'
import Testimonials from './components/Testimonials.vue'
import Contact from './components/Contact.vue'

const projects = [
  {
    title: 'Ecommerce Platform',
    desc: 'Spring Boot + Vue.js with migrations, catalog, checkout, admin dashboard.',
    stack: 'Spring Boot, Vue, MySQL',
    image: '/assets/projects/ecommerce.jpg',
    links: { case: '#', source: '#' }
  },
  {
    title: 'Job Portal',
    desc: 'Responsive job search UI with role-based auth and email alerts.',
    stack: 'Node, Vue, Sequelize',
    image: '/assets/projects/job-portal.jpg',
    links: { case: '#', source: '#' }
  },
  {
    title: 'Aneka Containers',
    desc: 'Local master/worker setup, stress tests, performance notes.',
    stack: 'Aneka, Windows',
    image: '/assets/projects/aneka.jpg',
    links: { case: '#', source: '#' }
  }
]
</script>

<style src="./styles.css"></style>

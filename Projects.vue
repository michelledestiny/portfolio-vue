<script setup>
defineProps({
  items: { type: Array, default: () => [] }
})
</script>

<template>
  <section id="projects" class="section">
    <div class="container">
      <h2>Projects</h2>
      <p class="section__intro">Selected work across full‑stack, cloud integration, and UI systems.</p>

      <div class="grid grid--3">
        <article v-for="(p,i) in items" :key="i" class="card project">
          <div class="card__media">
            <img :src="p.image" :alt="p.title" />
          </div>
          <div class="card__body">
            <h3 class="card__title">{{ p.title }}</h3>
            <p>{{ p.desc }}</p>
            <div class="card__meta"><strong>Stack:</strong> {{ p.stack }}</div>
            <div class="card__actions">
              <a :href="p.links.case" class="btn btn--sm btn--primary">Case study</a>
              <a :href="p.links.source" class="btn btn--sm btn--ghost">Source</a>
            </div>
          </div>
        </article>
      </div>

      <details class="details">
        <summary>See more projects</summary>
        <div class="grid grid--3">
          <article class="card project">
            <div class="card__media"><img src="/assets/projects/portfolio.jpg" alt="Portfolio UI" /></div>
            <div class="card__body">
              <h3 class="card__title">Portfolio System</h3>
              <p>Modular components, print CV, dark mode, and mobile-first nav.</p>
              <div class="card__meta"><strong>Stack:</strong> HTML, CSS</div>
              <div class="card__actions">
                <a href="#" class="btn btn--sm btn--primary">Case study</a>
                <a href="#" class="btn btn--sm btn--ghost">Source</a>
              </div>
            </div>
          </article>
        </div>
      </details>
    </div>
  </section>
</template>

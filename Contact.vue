<template>
  <section id="contact" class="section section--alt">
    <div class="container">
      <h2>Contact</h2>
      <p>Want to collaborate or learn together? I’m open to internships, junior roles, and community projects.</p>
      <form class="form" action="#" method="post" aria-label="Contact form">
        <div class="form__row">
          <label for="name">Name</label>
          <input id="name" name="name" type="text" placeholder="Your name" required />
        </div>
        <div class="form__row">
          <label for="email">Email</label>
          <input id="email" name="email" type="email" placeholder="you@example.com" required />
        </div>
        <div class="form__row">
          <label for="message">Message</label>
          <textarea id="message" name="message" rows="6" placeholder="Tell me about your project" required></textarea>
        </div>
        <button class="btn btn--primary" type="submit">Send</button>
        <p class="form__note">Note: This demo form needs backend wiring (Formspree or a simple server).</p>
      </form>
    </div>
  </section>
</template>

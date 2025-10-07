<template>
  <div class="home">
    <!-- Hero Section -->
    <section class="hero">
      <div class="container">
        <h1>You want it. I build it.</h1>
        <p>Custom, responsive websites tailored for your business—built to grow.</p>
        <router-link to="/contact" class="cta">Get a Free Quote</router-link>
      </div>
    </section>

    <!-- About/Services Section -->
    <section class="about">
      <div class="container">
        <h2>What I Build</h2>
        <p>I create clean, user-friendly websites for local businesses using modern tools like Vue.js, JavaScript, and CSS. No fluff—just code that works.</p>
        <ul class="services">
          <li>Responsive business websites</li>
          <li>Landing pages that convert</li>
          <li>Fast, SEO-friendly designs</li>
        </ul>
      </div>
    </section>

    <!-- Portfolio Section (Single Project) -->
    <section class="portfolio">
      <div class="container">
        <h2>My Work</h2>
        <p class="portfolio-intro">Scroll through to see examples of my business websites.</p>
        
        <!-- Single Project Card -->
        <article class="project">
          <img
            src="https://placehold.co/600x300/cccccc/333333?text=Business+Website+Mockup&font=montserrat"
            alt="Business Website Mockup"
            class="project-image"
            @error="handleImageError"
          />
          <div class="project-content">
            <h3>Business Website</h3>
            <p>A modern, responsive site for a local business, with clean design, contact forms, and SEO basics to boost online presence.</p>
            <p class="tech">Built with: HTML, CSS, JavaScript, Vue.js</p>
            <a href="#" class="project-link">View Details</a>
          </div>
        </article>
        <!-- Add more <article class="project">...</article> here for additional screenshots -->
      </div>
    </section>

    <!-- Contact Section -->
    <section class="contact">
      <div class="container">
        <h2>Let's Build Something</h2>
        <p>Ready to get started? Reach out today.</p>
        <button @click="copyEmail" class="cta">Copy Email: armeswebsites@gmail.com</button>
        <p>Or manually copy: <strong>armeswebsites@gmail.com</strong></p>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  methods: {
    async copyEmail() {
      const email = 'armeswebsites@gmail.com';
      try {
        await navigator.clipboard.writeText(email);
        alert('Email copied! Paste it into your client to chat about your project.');
      } catch (err) {
        console.error('Copy failed:', err);
        alert('Copy failed—select and copy manually.');
      }
    },
    handleImageError(event) {
      event.target.src = 'https://placehold.co/600x300/cccccc/333333?text=Project+Coming+Soon&font=montserrat';
    },
  },
};
</script>

<style scoped>
.home {
  scroll-behavior: smooth;
}
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 0 20px;
}
.hero {
  text-align: center;
  padding: 80px 20px;
  background: linear-gradient(to bottom, #f0f0f0, #e0e0e0);
}
.hero h1 {
  font-size: 2.8rem;
  margin-bottom: 10px;
  color: #333;
}
.hero p {
  font-size: 1.2rem;
  color: #555;
  margin-bottom: 30px;
}
.cta {
  display: inline-block;
  padding: 12px 24px;
  background: #007bff;
  color: white;
  text-decoration: none;
  border: none;
  border-radius: 5px;
  font-weight: bold;
  cursor: pointer;
  transition: background 0.3s;
}
.cta:hover {
  background: #0056b3;
}
.about {
  padding: 50px 20px;
  background: #fff;
  text-align: center;
}
.about h2 {
  font-size: 2.2rem;
  margin-bottom: 20px;
}
.about p {
  font-size: 1.1rem;
  color: #555;
  margin-bottom: 20px;
}
.services {
  list-style: none;
  padding: 0;
}
.services li {
  font-size: 1rem;
  color: #666;
  margin-bottom: 10px;
  padding-left: 20px;
  position: relative;
}
.services li::before {
  content: '→';
  position: absolute;
  left: 0;
  color: #007bff;
}
.portfolio {
  padding: 50px 20px;
  background: #f9f9f9;
}
.portfolio h2 {
  text-align: center;
  font-size: 2.2rem;
  margin-bottom: 10px;
}
.portfolio-intro {
  text-align: center;
  font-size: 1rem;
  color: #555;
  margin-bottom: 40px;
}
.project {
  display: flex;
  align-items: center;
  margin-bottom: 40px;
  background: #fff;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  transition: transform 0.3s;
}
.project:hover {
  transform: translateY(-5px);
}
.project-image {
  width: 50%;
  height: 300px;
  object-fit: cover;
}
.project-content {
  width: 50%;
  padding: 30px;
}
.project h3 {
  font-size: 1.8rem;
  margin-bottom: 10px;
  color: #333;
}
.project p {
  color: #666;
  line-height: 1.5;
  margin-bottom: 10px;
}
.tech {
  font-style: italic;
  color: #007bff;
  margin-bottom: 15px;
}
.project-link {
  color: #007bff;
  text-decoration: none;
  font-weight: bold;
}
.project-link:hover {
  text-decoration: underline;
}
.contact {
  padding: 50px 20px;
  text-align: center;
  background: #fff;
}
.contact h2 {
  font-size: 2.2rem;
  margin-bottom: 20px;
}
.contact p {
  font-size: 1.1rem;
  color: #555;
  margin-bottom: 20px;
}
@media (max-width: 768px) {
  .project {
    flex-direction: column;
  }
  .project-image {
    width: 100%;
    height: 200px;
  }
  .project-content {
    width: 100%;
    padding: 20px;
  }
  .hero h1 {
    font-size: 2.2rem;
  }
}
</style>
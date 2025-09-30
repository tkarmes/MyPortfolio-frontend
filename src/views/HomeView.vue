<template>
  <div class="hero">
    <h1>You want it. I Build it.</h1>
    <p>Custom websites and apps for your business</p>
    <router-link to="/contact" class="cta">Get a Free Quote</router-link>
  </div>
  <div class="portfolio-preview">
    <h2>Recent Work</h2>
    <div class="projects">
      <div class="project">
        <div class="placeholder-image">Business Website</div>
        <h3>Business Website</h3>
        <p>A modern, responsive website for a local retail store, boosting online presence.</p>
        <a href="#" class="project-link">View Project</a>
      </div>
      <div class="project">
        <div class="placeholder-image">E-Commerce App</div>
        <h3>E-Commerce App</h3>
        <p>A mobile-friendly app for seamless online shopping experiences.</p>
        <a href="#" class="project-link">View Project</a>
      </div>
      <div class="project">
        <div class="placeholder-image">Portfolio Site</div>
        <h3>Portfolio Site</h3>
        <p>A sleek personal portfolio to showcase client projects.</p>
        <a href="#" class="project-link">View Project</a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.hero {
  text-align: center;
  padding: 60px 20px;
  background: linear-gradient(to bottom, #f0f0f0, #e0e0e0);
}
.hero h1 {
  font-size: 2.5rem;
  margin-bottom: 10px;
}
.hero p {
  font-size: 1.2rem;
  color: #555;
}
.cta {
  display: inline-block;
  padding: 12px 24px;
  background: #007bff;
  color: white;
  text-decoration: none;
  border-radius: 5px;
  font-weight: bold;
  transition: background 0.3s;
}
.cta:hover {
  background: #0056b3;
}
.portfolio-preview {
  padding: 40px 20px;
  text-align: center;
  background: #fff;
}
.portfolio-preview h2 {
  font-size: 2rem;
  margin-bottom: 20px;
}
.projects {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 30px;
  max-width: 1200px;
  margin: 0 auto;
}
.project {
  background: #f9f9f9;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s;
}
.project:hover {
  transform: translateY(-5px);
}
.placeholder-image {
  width: 100%;
  height: 150px;
  background: #ccc;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 5px;
  margin-bottom: 10px;
  color: #333;
  font-weight: bold;
}
.project h3 {
  font-size: 1.5rem;
  margin: 10px 0;
}
.project p {
  color: #666;
  font-size: 1rem;
}
.project-link {
  display: inline-block;
  margin-top: 10px;
  color: #007bff;
  text-decoration: none;
  font-weight: bold;
}
.project-link:hover {
  text-decoration: underline;
}
</style>
<template>
  <div class="home">
    <!-- Hero Section -->
    <section class="hero">
      <div class="container">
        <h1>You want it. I build it.</h1>
        <p>Custom, responsive websites tailored for your business—built to grow.</p>
        <a href="#contact" class="cta">Get a Free Quote</a>
      </div>
    </section>

    <!-- About/Services Section -->
    <section class="about">
      <div class="container">
        <h2>What I Build</h2>
        <p>I create clean, user-friendly websites for local businesses in Tyler and Cedar Creek Lake using Vue.js, JavaScript, and CSS. No fluff—just code that works.</p>
        <ul class="services">
          <li>Responsive business websites</li>
          <li>Landing pages that convert</li>
          <li>Fast, SEO-friendly designs</li>
        </ul>
      </div>
    </section>

    <!-- Portfolio Section (Ten Projects) -->
    <section class="portfolio">
      <div class="container">
        <h2>My Work</h2>
        <p class="portfolio-intro">Scroll through to see examples of my business websites.</p>
        
        <!-- Project 1: Tyler Furniture -->
        <article class="project">
          <img
            src="@/assets/tyler-furniture.jpg"
            alt="Tyler Furniture Co. Website Mockup"
            class="project-image"
            @error="handleImageError"
          />
          <div class="project-content">
            <h3>Tyler Furniture Co.</h3>
            <p>A bold, responsive website for a Tyler, TX furniture store, featuring a modern hero, product grid, and sticky navigation for a premium user experience.</p>
            <p class="tech">Built with: HTML, CSS, JavaScript</p>
            <a href="#" class="project-link">View Details</a>
          </div>
        </article>

        <!-- Project 2: Cedar Creek Drywall -->
        <article class="project">
          <img
            src="@/assets/cedar-creek-drywall.jpg"
            alt="Cedar Creek Drywall Website Mockup"
            class="project-image"
            @error="handleImageError"
          />
          <div class="project-content">
            <h3>Cedar Creek Drywall</h3>
            <p>A rugged, responsive site for a sheetrock contractor at Cedar Creek Lake, with fixed nav tabs, a drywall texture background, and real construction images.</p>
            <p class="tech">Built with: HTML, CSS, JavaScript</p>
            <a href="#" class="project-link">View Details</a>
          </div>
        </article>

        <!-- Project 3: Cedar Creek Drywall -->
        <article class="project">
          <img
            src="@/assets/cedar-creek-drywall-2.jpg"
            alt="Cedar Creek Drywall Website Mockup"
            class="project-image"
            @error="handleImageError"
          />
          <div class="project-content">
            <h3>Cedar Creek Drywall</h3>
            <p>A fresh take on the sheetrock contractor site for Cedar Creek Lake, with a unique layout and enhanced visuals for local lakefront clients.</p>
            <p class="tech">Built with: HTML, CSS, JavaScript</p>
            <a href="#" class="project-link">View Details</a>
          </div>
        </article>

        <!-- Project 4: Martinez Bros. Irrigation -->
        <article class="project">
          <img
            src="@/assets/martinez-bros-irrigation.jpg"
            alt="Martinez Bros. Irrigation Website Mockup"
            class="project-image"
            @error="handleImageError"
          />
          <div class="project-content">
            <h3>Martinez Bros. Irrigation</h3>
            <p>A responsive website for an East Texas irrigation company, featuring a fixed top navigation, lush lawn imagery, and a clean service grid for showcasing sprinkler and lawn care services.</p>
            <p class="tech">Built with: HTML, CSS, JavaScript</p>
            <a href="/demos/martinez-bros-irrigation.html" class="project-link">View Demo</a>
          </div>
        </article>

        <!-- Project 5: Martinez Bros. Irrigation -->
        <article class="project">
          <img
            src="@/assets/martinez-bros-irrigation-2.jpg"
            alt="Martinez Bros. Irrigation Website Mockup"
            class="project-image"
            @error="handleImageError"
          />
          <div class="project-content">
            <h3>Martinez Bros. Irrigation</h3>
            <p>A unique take on the irrigation site with a bottom navigation bar, circular service cards, and a diagonal section tilt, showcasing a modern, dynamic layout for East Texas clients.</p>
            <p class="tech">Built with: HTML, CSS, JavaScript</p>
            <a href="/demos/martinez-bros-irrigation.html" class="project-link">View Demo</a>
          </div>
        </article>

        <!-- Project 6: Lakeview Coffee Co. -->
        <article class="project">
          <img
            src="@/assets/lakeview-coffee.jpg"
            alt="Lakeview Coffee Co. Website Mockup"
            class="project-image"
            @error="handleImageError"
          />
          <div class="project-content">
            <h3>Lakeview Coffee Co.</h3>
            <p>A vibrant website for a Tyler, TX coffee shop, featuring a full-screen overlay menu with animated links, a split-screen hero with a large cozy coffee shop image, and a carousel slider for the menu.</p>
            <p class="tech">Built with: HTML, CSS, JavaScript</p>
            <a href="/demos/lakeview-coffee.html" class="project-link">View Demo</a>
          </div>
        </article>

        <!-- Project 7: Lakeview Coffee Co. -->
        <article class="project">
          <img
            src="@/assets/lakeview-coffee-2.jpg"
            alt="Lakeview Coffee Co. Website Mockup"
            class="project-image"
            @error="handleImageError"
          />
          <div class="project-content">
            <h3>Lakeview Coffee Co.</h3>
            <p>A dynamic take on the Tyler, TX coffee shop site, emphasizing the split-screen hero with right-aligned text and a carousel showcasing artisanal coffee and pastries.</p>
            <p class="tech">Built with: HTML, CSS, JavaScript</p>
            <a href="/demos/lakeview-coffee.html" class="project-link">View Demo</a>
          </div>
        </article>

        <!-- Project 8: Lakeview Coffee Co. -->
        <article class="project">
          <img
            src="@/assets/lakeview-coffee-3.jpg"
            alt="Lakeview Coffee Co. Website Mockup"
            class="project-image"
            @error="handleImageError"
          />
          <div class="project-content">
            <h3>Lakeview Coffee Co.</h3>
            <p>A fresh iteration of the coffee shop website, highlighting a fixed contact bar and a cozy aesthetic with a prominent background image for Tyler, TX clients.</p>
            <p class="tech">Built with: HTML, CSS, JavaScript</p>
            <a href="/demos/lakeview-coffee.html" class="project-link">View Demo</a>
          </div>
        </article>

        <!-- Project 9: East Texas Tavern -->
        <article class="project">
          <img
            src="@/assets/east-texas-tavern.jpg"
            alt="East Texas Tavern Website Mockup"
            class="project-image"
            @error="handleImageError"
          />
          <div class="project-content">
            <h3>East Texas Tavern</h3>
            <p>A modern website for a Tyler, TX bar, featuring a parallax scrolling hero, sticky navigation, tabbed menu for drinks and events, and a fixed social media footer.</p>
            <p class="tech">Built with: HTML, CSS, JavaScript</p>
            <a href="/demos/east-texas-tavern.html" class="project-link">View Demo</a>
          </div>
        </article>

        <!-- Project 10: East Texas Tavern -->
        <article class="project">
          <img
            src="@/assets/east-texas-tavern-2.jpg"
            alt="East Texas Tavern Website Mockup"
            class="project-image"
            @error="handleImageError"
          />
          <div class="project-content">
            <h3>East Texas Tavern</h3>
            <p>A vibrant take on the Tyler, TX bar website, showcasing a scrolling marquee for live music events in the tabbed menu, paired with a gritty, rustic aesthetic.</p>
            <p class="tech">Built with: HTML, CSS, JavaScript</p>
            <a href="/demos/east-texas-tavern.html" class="project-link">View Demo</a>
          </div>
        </article>
      </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
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
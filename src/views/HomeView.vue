<!-- Home.vue (or whichever file this component is in) -->
<template>
  <div class="home">
    <!-- Header Section with Navigation -->
    <header class="header">
      <h1>Web Rousers</h1>
      <nav class="nav">
        <a href="#home">Home</a>
        <a href="#about">Services</a>
        <a href="#portfolio">Portfolio</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
      <div class="hero-content">
        <h1>You Want It. I Build It.</h1>
        <p>Custom, responsive websites tailored for your business—built to grow your brand.</p>
        <button @click="openContactModal" class="cta">Get a Free Quote</button>
      </div>
    </section>

    <!-- About/Services Section -->
    <section class="about" id="about">
      <div class="container">
        <h2>What I Build</h2>
        <p class="about-intro">I craft clean, user-friendly websites for businesses.</p>
        <div class="services-carousel">
          <div class="services-track">
            <!-- Original cards -->
            <div class="service-card">
              <h3>Responsive Websites</h3>
              <p>Sites that look great on any device, from phones to desktops.</p>
            </div>
            <div class="service-card">
              <h3>Landing Pages</h3>
              <p>High-converting pages designed to drive customer action.</p>
            </div>
            <div class="service-card">
              <h3>SEO-Friendly Designs</h3>
              <p>Optimized to rank higher and attract clients.</p>
            </div>
            <!-- Cloned cards -->
            <div class="service-card">
              <h3>Responsive Websites</h3>
              <p>Sites that look great on any device, from phones to desktops.</p>
            </div>
            <div class="service-card">
              <h3>Landing Pages</h3>
              <p>High-converting pages designed to drive customer action.</p>
            </div>
            <div class="service-card">
              <h3>SEO-Friendly Designs</h3>
              <p>Optimized to rank higher and attract clients.</p>
            </div>
          </div>
          <button class="carousel-btn service-prev-btn">←</button>
          <button class="carousel-btn service-next-btn">→</button>
        </div>
      </div>
    </section>

    <!-- Portfolio Section -->
    <section class="portfolio" id="portfolio">
      <div class="container">
        <h2>My Work</h2>
        <p class="portfolio-intro">Click the arrows to explore my business websites.</p>
        <div class="carousel">
          <div class="carousel-track">
            <!-- Original projects -->
            <article class="project">
              <img :src="images.tylerFurniture" alt="Furniture Co. Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Furniture Co.</h3>
                <p>A bold, responsive website for a furniture store, featuring a modern hero, product grid, and sticky navigation for a premium user experience.</p>
                <button @click="openImageModal(images.tylerFurniture)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.cedarCreekDrywall" alt="Drywall Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Drywall</h3>
                <p>A rugged, responsive site for a sheetrock contractor, with fixed nav tabs, a drywall texture background, and real construction images.</p>
                <button @click="openImageModal(images.cedarCreekDrywall)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.cedarCreekDrywall2" alt="Drywall Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Drywall</h3>
                <p>A fresh take on the sheetrock contractor site, with a unique layout and enhanced visuals for clients.</p>
                <button @click="openImageModal(images.cedarCreekDrywall2)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.martinezBrosIrrigation" alt="Irrigation Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Irrigation</h3>
                <p>A responsive website for an irrigation company, featuring a fixed top navigation, lush lawn imagery, and a clean service grid for showcasing sprinkler and lawn care services.</p>
                <button @click="openImageModal(images.martinezBrosIrrigation)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.martinezBrosIrrigation2" alt="Irrigation Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Irrigation</h3>
                <p>A unique take on the irrigation site with a bottom navigation bar, circular service cards, and a diagonal section tilt, showcasing a modern, dynamic layout.</p>
                <button @click="openImageModal(images.martinezBrosIrrigation2)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.lakeviewCoffee" alt="Coffee Co. Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Coffee Co.</h3>
                <p>A vibrant website for a coffee shop, featuring a full-screen overlay menu with animated links, a split-screen hero with a large cozy coffee shop image, and a carousel slider for the menu.</p>
                <button @click="openImageModal(images.lakeviewCoffee)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.lakeviewCoffee2" alt="Coffee Co. Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Coffee Co.</h3>
                <p>A dynamic take on the coffee shop site, emphasizing the split-screen hero with right-aligned text and a carousel showcasing artisanal coffee and pastries.</p>
                <button @click="openImageModal(images.lakeviewCoffee2)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.lakeviewCoffee3" alt="Coffee Co. Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Coffee Co.</h3>
                <p>A fresh iteration of the coffee shop website, highlighting a fixed contact bar and a cozy aesthetic with a prominent background image.</p>
                <button @click="openImageModal(images.lakeviewCoffee3)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.eastTexasTavern" alt="Tavern Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Tavern</h3>
                <p>A modern website for a bar, featuring a parallax scrolling hero, sticky navigation, tabbed menu for drinks and events, and a fixed social media footer.</p>
                <button @click="openImageModal(images.eastTexasTavern)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.eastTexasTavern2" alt="Tavern Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Tavern</h3>
                <p>A vibrant take on the bar website, showcasing a scrolling marquee for live music events in the tabbed menu, paired with a gritty, rustic aesthetic.</p>
                <button @click="openImageModal(images.eastTexasTavern2)" class="project-link">View Details</button>
              </div>
            </article>
            <!-- Cloned projects -->
            <article class="project">
              <img :src="images.tylerFurniture" alt="Furniture Co. Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Furniture Co.</h3>
                <p>A bold, responsive website for a furniture store, featuring a modern hero, product grid, and sticky navigation for a premium user experience.</p>
                <button @click="openImageModal(images.tylerFurniture)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.cedarCreekDrywall" alt="Drywall Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Drywall</h3>
                <p>A rugged, responsive site for a sheetrock contractor, with fixed nav tabs, a drywall texture background, and real construction images.</p>
                <button @click="openImageModal(images.cedarCreekDrywall)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.cedarCreekDrywall2" alt="Drywall Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Drywall</h3>
                <p>A fresh take on the sheetrock contractor site, with a unique layout and enhanced visuals for clients.</p>
                <button @click="openImageModal(images.cedarCreekDrywall2)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.martinezBrosIrrigation" alt="Irrigation Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Irrigation</h3>
                <p>A responsive website for an irrigation company, featuring a fixed top navigation, lush lawn imagery, and a clean service grid for showcasing sprinkler and lawn care services.</p>
                <button @click="openImageModal(images.martinezBrosIrrigation)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.martinezBrosIrrigation2" alt="Irrigation Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Irrigation</h3>
                <p>A unique take on the irrigation site with a bottom navigation bar, circular service cards, and a diagonal section tilt, showcasing a modern, dynamic layout.</p>
                <button @click="openImageModal(images.martinezBrosIrrigation2)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.lakeviewCoffee" alt="Coffee Co. Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Coffee Co.</h3>
                <p>A vibrant website for a coffee shop, featuring a full-screen overlay menu with animated links, a split-screen hero with a large cozy coffee shop image, and a carousel slider for the menu.</p>
                <button @click="openImageModal(images.lakeviewCoffee)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.lakeviewCoffee2" alt="Coffee Co. Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Coffee Co.</h3>
                <p>A dynamic take on the coffee shop site, emphasizing the split-screen hero with right-aligned text and a carousel showcasing artisanal coffee and pastries.</p>
                <button @click="openImageModal(images.lakeviewCoffee2)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.lakeviewCoffee3" alt="Coffee Co. Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Coffee Co.</h3>
                <p>A fresh iteration of the coffee shop website, highlighting a fixed contact bar and a cozy aesthetic with a prominent background image.</p>
                <button @click="openImageModal(images.lakeviewCoffee3)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.eastTexasTavern" alt="Tavern Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Tavern</h3>
                <p>A modern website for a bar, featuring a parallax scrolling hero, sticky navigation, tabbed menu for drinks and events, and a fixed social media footer.</p>
                <button @click="openImageModal(images.eastTexasTavern)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.eastTexasTavern2" alt="Tavern Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Tavern</h3>
                <p>A vibrant take on the bar website, showcasing a scrolling marquee for live music events in the tabbed menu, paired with a gritty, rustic aesthetic.</p>
                <button @click="openImageModal(images.eastTexasTavern2)" class="project-link">View Details</button>
              </div>
            </article>
          </div>
          <button class="carousel-btn prev-btn">←</button>
          <button class="carousel-btn next-btn">→</button>
        </div>
      </div>
    </section>

    <!-- Image Modal -->
    <div v-if="showModal" class="modal">
      <div class="modal-content">
        <span class="modal-close" @click="closeImageModal">&times;</span>
        <img :src="modalImage" alt="Enlarged Project Image" class="modal-image" />
      </div>
    </div>

    <!-- Contact Modal -->
    <div v-if="showContactModal" class="modal contact-modal">
      <div class="modal-content">
        <span class="modal-close" @click="closeContactModal">&times;</span>
        <h2>Let's Build Something</h2>
        <p>Fill out the form or copy my email to get started.</p>
        <form class="contact-form" @submit.prevent="submitContactForm">
          <input type="text" v-model="contactForm.name" placeholder="Your Name" required />
          <input type="email" v-model="contactForm.email" placeholder="Your Email" required />
          <textarea v-model="contactForm.message" placeholder="Your Message" required></textarea>
          <button type="submit" class="cta">Send Message</button>
        </form>
        <button @click="copyEmail" class="cta email-copy">Copy Email: armeswebsites@gmail.com</button>
      </div>
    </div>

    <!-- Contact Section -->
    <section class="contact" id="contact">
      <div class="container">
        <h2>Ready to Start?</h2>
        <p>Contact me to bring your website vision to life.</p>
        <button @click="openContactModal" class="cta">Get in Touch</button>
      </div>
    </section>
  </div>
</template>

<script>
import tylerFurniture from '@/assets/tyler-furniture.jpg';
import cedarCreekDrywall from '@/assets/cedar-creek-drywall.jpg';
import cedarCreekDrywall2 from '@/assets/cedar-creek-drywall-2.jpg';
import martinezBrosIrrigation from '@/assets/martinez-bros-irrigation.jpg';
import martinezBrosIrrigation2 from '@/assets/martinez-bros-irrigation-2.jpg';
import lakeviewCoffee from '@/assets/lakeview-coffee.jpg';
import lakeviewCoffee2 from '@/assets/lakeview-coffee-2.jpg';
import lakeviewCoffee3 from '@/assets/lakeview-coffee-3.jpg';
import eastTexasTavern from '@/assets/east-texas-tavern.jpg';
import eastTexasTavern2 from '@/assets/east-texas-tavern-2.jpg';

export default {
  data() {
    return {
      showModal: false,
      modalImage: '',
      showContactModal: false,
      contactForm: {
        name: '',
        email: '',
        message: '',
      },
      images: {
        tylerFurniture,
        cedarCreekDrywall,
        cedarCreekDrywall2,
        martinezBrosIrrigation,
        martinezBrosIrrigation2,
        lakeviewCoffee,
        lakeviewCoffee2,
        lakeviewCoffee3,
        eastTexasTavern,
        eastTexasTavern2,
      },
    };
  },
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
      event.target.src = 'https://placehold.co/600x300/1A1A1A/FFFFFF?text=Project+Coming+Soon&font=montserrat';
    },
    initCarousel() {
      const track = document.querySelector('.carousel-track');
      const items = document.querySelectorAll('.project');
      const prevBtn = document.querySelector('.prev-btn');
      const nextBtn = document.querySelector('.next-btn');
      const totalItems = items.length / 2; // 10 original projects
      let currentIndex = 1; // Start at first original project

      function updateCarousel(transition = true) {
        track.style.transition = transition ? 'transform 0.5s ease' : 'none';
        track.style.transform = `translateX(-${(currentIndex * 100) / items.length}%)`;
      }

      nextBtn.addEventListener('click', () => {
        currentIndex++;
        updateCarousel();
        if (currentIndex === totalItems + 1) {
          setTimeout(() => {
            currentIndex = 1;
            updateCarousel(false);
          }, 500); // Match transition duration
        }
      });

      prevBtn.addEventListener('click', () => {
        currentIndex--;
        updateCarousel();
        if (currentIndex === 0) {
          setTimeout(() => {
            currentIndex = totalItems;
            updateCarousel(false);
          }, 500); // Match transition duration
        }
      });

      // Auto-scroll
      let autoScrollInterval = setInterval(() => {
        currentIndex++;
        updateCarousel();
        if (currentIndex === totalItems + 1) {
          currentIndex = 1;
          updateCarousel(false);
        }
      }, 3000); // 3 seconds per slide

      // Pause on hover
      track.parentElement.addEventListener('mouseenter', () => clearInterval(autoScrollInterval));
      track.parentElement.addEventListener('mouseleave', () => {
        autoScrollInterval = setInterval(() => {
          currentIndex++;
          updateCarousel();
          if (currentIndex === totalItems + 1) {
            currentIndex = 1;
            updateCarousel(false);
          }
        }, 3000);
      });

      this.$nextTick(() => {
        updateCarousel(false); // Initial position without transition
      });
    },
    initServicesCarousel() {
      const track = document.querySelector('.services-track');
      const items = document.querySelectorAll('.service-card');
      const prevBtn = document.querySelector('.service-prev-btn');
      const nextBtn = document.querySelector('.service-next-btn');
      const totalItems = items.length / 2; // 3 original cards
      let currentIndex = 1; // Start at first original card

      function updateCarousel(transition = true) {
        track.style.transition = transition ? 'transform 0.7s ease' : 'none';
        track.style.transform = `translateX(-${(currentIndex * 100) / items.length}%)`;
      }

      nextBtn.addEventListener('click', () => {
        currentIndex++;
        updateCarousel();
        if (currentIndex === totalItems + 1) {
          setTimeout(() => {
            currentIndex = 1;
            updateCarousel(false);
          }, 700); // Match transition duration
        }
      });

      prevBtn.addEventListener('click', () => {
        currentIndex--;
        updateCarousel();
        if (currentIndex === 0) {
          setTimeout(() => {
            currentIndex = totalItems;
            updateCarousel(false);
          }, 700); // Match transition duration
        }
      });

      // Auto-scroll
      let autoScrollInterval = setInterval(() => {
        currentIndex++;
        updateCarousel();
        if (currentIndex === totalItems + 1) {
          currentIndex = 1;
          updateCarousel(false);
        }
      }, 3000); // 3 seconds per slide

      // Pause on hover
      track.parentElement.addEventListener('mouseenter', () => clearInterval(autoScrollInterval));
      track.parentElement.addEventListener('mouseleave', () => {
        autoScrollInterval = setInterval(() => {
          currentIndex++;
          updateCarousel();
          if (currentIndex === totalItems + 1) {
            currentIndex = 1;
            updateCarousel(false);
          }
        }, 3000);
      });

      this.$nextTick(() => {
        updateCarousel(false); // Initial position without transition
      });
    },
    openImageModal(image) {
      this.modalImage = image;
      this.showModal = true;
    },
    closeImageModal() {
      this.showModal = false;
      this.modalImage = '';
    },
    openContactModal() {
      this.showContactModal = true;
    },
    closeContactModal() {
      this.showContactModal = false;
      this.contactForm = { name: '', email: '', message: '' };
    },
    submitContactForm() {
      alert('Form submitted! I’ll get back to you soon.');
      this.closeContactModal();
    },
  },
  mounted() {
    this.initCarousel();
    this.initServicesCarousel();
  },
};
</script>

<style scoped>
/* Global Styles */
.home {
  scroll-behavior: smooth;
  font-family: 'Montserrat', sans-serif;
  background: var(--background);
  color: var(--text);
}

/* Header Section */
.header {
  text-align: center;
  padding: 20px 0;
  background: var(--background);
}
.header h1 {
  font-size: 3rem;
  font-weight: 700;
  color: var(--primary);
  text-transform: uppercase;
  margin: 0;
  letter-spacing: 2px;
  transition: color 0.3s ease;
}
.header h1:hover {
  color: var(--secondary);
}
.nav {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin-top: 10px;
}
.nav a {
  color: var(--text);
  text-decoration: none;
  font-weight: bold;
  transition: color 0.3s;
}
.nav a:hover {
  color: var(--primary);
}

/* Container */
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Hero Section */
.hero {
  height: 80vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--background);
  text-align: center;
  animation: fadeIn 1s ease-in;
}
.hero-content {
  padding: 40px;
}
.hero h1 {
  font-size: 4rem;
  font-weight: 700;
  margin-bottom: 20px;
  color: var(--text);
  text-transform: uppercase;
}
.hero p {
  font-size: 1.5rem;
  margin-bottom: 30px;
  color: var(--text);
}
.cta {
  display: inline-block;
  padding: 12px 24px;
  background: var(--primary);
  color: var(--text);
  text-decoration: none;
  border: none;
  border-radius: 5px;
  font-weight: bold;
  cursor: pointer;
  transition: transform 0.3s, background 0.3s;
}
.cta:hover {
  background: var(--accent);
  transform: scale(1.05);
}

/* Fade-in Animation */
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* About Section */
.about {
  padding: 80px 20px;
  background: var(--text);
}
.about h2 {
  font-size: 2.5rem;
  margin-bottom: 20px;
  color: var(--background);
  text-transform: uppercase;
}
.about-intro {
  font-size: 1.2rem;
  color: var(--background);
  margin-bottom: 40px;
}
.services-carousel {
  position: relative;
  overflow: hidden;
  max-width: 600px;
  margin: 0 auto;
}
.services-track {
  display: flex;
  width: 600%; /* 6 cards (3 original + 3 clones) */
}
.service-card {
  flex: 0 0 16.6667%; /* 100% / 6 */
  background: var(--background);
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
  box-sizing: border-box;
  transition: border 0.3s;
}
.service-card:hover {
  border: 2px solid var(--primary);
}
.service-card h3 {
  font-size: 1.5rem;
  margin-bottom: 10px;
  color: var(--secondary);
}
.service-card p {
  font-size: 1rem;
  color: var(--text);
}
.carousel-btn {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: var(--primary);
  color: var(--text);
  border: none;
  padding: 10px;
  cursor: pointer;
  font-size: 1.5rem;
  border-radius: 50%;
  transition: background 0.3s;
}
.carousel-btn:hover {
  background: var(--accent);
}
.service-prev-btn {
  left: 10px;
}
.service-next-btn {
  right: 10px;
}

/* Portfolio Section */
.portfolio {
  padding: 80px 20px;
  background: var(--background);
}
.portfolio h2 {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 10px;
  color: var(--text);
  text-transform: uppercase;
}
.portfolio-intro {
  text-align: center;
  font-size: 1rem;
  color: var(--text);
  margin-bottom: 40px;
}
.carousel {
  position: relative;
  overflow: hidden;
}
.carousel-track {
  display: flex;
  width: 2000%; /* 20 projects (10 original + 10 clones) */
  animation-play-state: running; /* Default for auto-scroll */
  animation-play-state: var(--auto-scroll-pause, running);
}
.project {
  flex: 0 0 5%; /* 100% / 20 */
  display: flex;
  align-items: center;
  background: var(--background);
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
  overflow: hidden;
  transition: transform 0.3s, border 0.3s;
}
.project:hover {
  transform: translateY(-5px);
  border: 2px solid var(--primary);
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
  color: var(--text);
}
.project p {
  color: var(--text);
  line-height: 1.5;
  margin-bottom: 10px;
}
.project-link {
  display: inline-block;
  padding: 8px 16px;
  background: var(--primary);
  color: var(--text);
  text-decoration: none;
  border-radius: 5px;
  font-weight: bold;
  cursor: pointer;
  transition: background 0.3s, transform 0.3s;
}
.project-link:hover {
  background: var(--accent);
  transform: scale(1.05);
}
.carousel-btn.prev-btn {
  left: 10px;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.3s ease;
}
.carousel-btn.next-btn {
  right: 10px;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.3s ease;
}
.carousel:hover .carousel-btn.prev-btn,
.carousel:hover .carousel-btn.next-btn {
  opacity: 1;
  pointer-events: auto;
}
@media (hover: none) {
  .carousel-btn.prev-btn,
  .carousel-btn.next-btn {
    opacity: 1;
    pointer-events: auto;
  }
}

/* Modal (Image and Contact) */
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.9);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}
.modal-content {
  position: relative;
  max-width: 80vw;
  max-height: 80vh;
}
.modal-image {
  width: 100%;
  height: auto;
  border-radius: 10px;
  border: 2px solid var(--secondary);
}
.modal-close {
  position: absolute;
  top: -30px;
  right: -30px;
  font-size: 2rem;
  color: var(--secondary);
  cursor: pointer;
  transition: color 0.3s;
}
.modal-close:hover {
  color: var(--primary);
}
.contact-modal .modal-content {
  background: var(--text);
  padding: 40px;
  border-radius: 10px;
  text-align: center;
  border: 2px solid var(--secondary);
}
.contact-modal h2 {
  font-size: 2rem;
  margin-bottom: 20px;
  color: var(--background);
}
.contact-modal p {
  font-size: 1.1rem;
  color: var(--background);
  margin-bottom: 20px;
}
.contact-form {
  display: flex;
  flex-direction: column;
  gap: 15px;
  margin-bottom: 20px;
}
.contact-form input,
.contact-form textarea {
  padding: 10px;
  border: 1px solid var(--background);
  border-radius: 5px;
  font-size: 1rem;
  background: var(--text);
  color: var(--background);
}
.contact-form textarea {
  height: 100px;
  resize: none;
}
.email-copy {
  margin-top: 10px;
  background: var(--primary);
}
.email-copy:hover {
  background: var(--accent);
}

/* Contact Section */
.contact {
  padding: 80px 20px;
  background: var(--background);
}
.contact h2 {
  font-size: 2.5rem;
  margin-bottom: 20px;
  color: var(--text);
  text-transform: uppercase;
}
.contact p {
  font-size: 1.2rem;
  margin-bottom: 30px;
  color: var(--text);
}

/* Responsive */
@media (max-width: 768px) {
  .header h1 {
    font-size: 2rem;
  }
  .nav {
    flex-direction: column;
    gap: 10px;
  }
  .hero h1 {
    font-size: 2.5rem;
  }
  .hero p {
    font-size: 1.2rem;
  }
  .hero {
    height: 70vh;
  }
  .about h2 {
    font-size: 2rem;
  }
  .services-carousel {
    max-width: 100%;
  }
  .service-prev-btn {
    left: 5px;
  }
  .service-next-btn {
    right: 5px;
  }
  .service-card {
    flex: 0 0 16.6667%;
  }
  .portfolio h2 {
    font-size: 2rem;
  }
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
  .carousel-btn.prev-btn {
    left: 5px;
    opacity: 1;
    pointer-events: auto;
  }
  .carousel-btn.next-btn {
    right: 5px;
    opacity: 1;
    pointer-events: auto;
  }
  .contact h2 {
    font-size: 2rem;
  }
  .modal-content {
    max-width: 90vw;
  }
  .modal-close {
    top: -20px;
    right: -20px;
    font-size: 1.5rem;
  }
}
</style>
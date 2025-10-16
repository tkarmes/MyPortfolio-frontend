<!-- Home.vue - SIMPLIFIED CONTACT READY -->
<template>
  <div class="home">
    <!-- Header Section with Navigation -->
    <header class="header">
      <div class="header-container">
        <nav class="nav nav-left">
          <a href="#home">Home</a>
          <a href="#about">Services</a>
        </nav>
        <a href="#home" class="logo-link">
          <img :src="images.webRousersLogo" alt="Web Rousers Logo" class="header-logo" @error="handleImageError" />
        </a>
        <nav class="nav nav-right">
          <a href="#portfolio">Portfolio</a>
          <a href="#contact">Contact</a>
        </nav>
      </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
      <div class="hero-background"></div>
      <div class="hero-content">
        <h1>You Want It. We Build It.</h1>
        <p>Custom, responsive websites tailored for your business—built to grow your brand.</p>
        <button @click="clickCTA" class="cta">Get a Free Quote</button>
      </div>
    </section>

    <!-- About/Services Section -->
    <section class="about" id="about">
      <div class="container">
        <h2>What We Build</h2>
        <p class="about-intro">We craft clean, user-friendly websites for businesses.</p>
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
        <h2>Our Work</h2>
        <p class="portfolio-intro">Click the arrows to explore our business websites.</p>
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

    <!-- Contact Modal - SIMPLIFIED -->
    <div v-if="showContactModal" class="modal contact-modal">
      <div class="modal-content">
        <span class="modal-close" @click="closeContactModal">&times;</span>
        <h2>Let's Build Something</h2>
        <div class="contact-info">
          <div class="contact-item">
            <span class="contact-icon">📧</span>
            <div>
              <strong>Email:</strong><br>
              <span class="copyable">armeswebsites@gmail.com</span>
            </div>
          </div>
          <div class="contact-item">
            <span class="contact-icon">📱</span>
            <div>
              <strong>Phone:</strong><br>
              <span class="copyable">(214) 548-3544</span>
            </div>
          </div>
        </div>
        <p class="contact-note">Just copy & paste to email/text us!</p>
      </div>
    </div>

    <!-- Contact Section -->
    <section class="contact" id="contact">
      <div class="container">
        <h2>Ready to Start?</h2>
        <p>Contact us to bring your website vision to life.</p>
        <button @click="clickCTA" class="cta">Get in Touch</button>
        <div class="footer-logo">
          <img :src="images.webRousersLogo" alt="Web Rousers Footer Logo" class="footer-logo-img" @error="handleImageError" />
        </div>
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
import webRousersLogo from '@/assets/web-rousers-logo-2.png';

export default {
  data() {
    return {
      showModal: false,
      modalImage: '',
      showContactModal: false,
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
        webRousersLogo,
      },
    };
  },
  methods: {
    clickCTA() {
      confetti({
        particleCount: 100,
        spread: 70,
        origin: { y: 0.6 },
        colors: ['#FFD700', '#FFA500', '#FF6347']
      });
      setTimeout(() => {
        this.openContactModal();
      }, 500);
    },
    handleImageError(event) {
      if (event.target.classList.contains('header-logo') || event.target.classList.contains('footer-logo-img')) {
        event.target.src = 'https://placehold.co/150x60/2F4F2F/F5F5DC?text=Logo+Error&font=montserrat';
      } else {
        event.target.src = 'https://placehold.co/600x300/2F4F2F/F5F5DC?text=Project+Coming+Soon&font=montserrat';
      }
    },

    initCarousel() {
      const track = document.querySelector('.carousel-track');
      const items = document.querySelectorAll('.project');
      const prevBtn = document.querySelector('.prev-btn');
      const nextBtn = document.querySelector('.next-btn');
      const totalItems = items.length / 2;
      let currentIndex = 1;

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
          }, 500);
        }
      });

      prevBtn.addEventListener('click', () => {
        currentIndex--;
        updateCarousel();
        if (currentIndex === 0) {
          setTimeout(() => {
            currentIndex = totalItems;
            updateCarousel(false);
          }, 500);
        }
      });

      let autoScrollInterval = setInterval(() => {
        currentIndex++;
        updateCarousel();
        if (currentIndex === totalItems + 1) {
          currentIndex = 1;
          updateCarousel(false);
        }
      }, 3000);

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
        updateCarousel(false);
      });
    },

    initServicesCarousel() {
      const track = document.querySelector('.services-track');
      const items = document.querySelectorAll('.service-card');
      const prevBtn = document.querySelector('.service-prev-btn');
      const nextBtn = document.querySelector('.service-next-btn');
      const totalItems = items.length / 2;
      let currentIndex = 1;

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
          }, 700);
        }
      });

      prevBtn.addEventListener('click', () => {
        currentIndex--;
        updateCarousel();
        if (currentIndex === 0) {
          setTimeout(() => {
            currentIndex = totalItems;
            updateCarousel(false);
          }, 700);
        }
      });

      let autoScrollInterval = setInterval(() => {
        currentIndex++;
        updateCarousel();
        if (currentIndex === totalItems + 1) {
          currentIndex = 1;
          updateCarousel(false);
        }
      }, 3000);

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
        updateCarousel(false);
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
    }
  },
  mounted() {
    this.initCarousel();
    this.initServicesCarousel();
  }
};
</script>

<style scoped>
/* Global Styles */
.home {
  scroll-behavior: smooth;
  font-family: 'Montserrat', sans-serif;
  color: var(--text);
}

/* Header Section */
.header {
  text-align: center;
  padding: 20px 0;
  background: rgba(255, 255, 255, 0.7);
  display: flex;
  justify-content: center;
  align-items: center;
}

.header-container {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 20px;
  max-width: 1200px;
  width: 100%;
}

.logo-link {
  display: inline-block;
  text-decoration: none;
}

.header-logo {
  max-height: 280px;
  width: auto;
  filter: hue-rotate(350deg) saturate(3) brightness(1.3);
  transition: all 0.3s ease;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
  animation: logoFadeIn 1s ease-in, logoGlow 2s ease-in-out infinite alternate;
}

.header-logo:hover {
  transform: scale(1.1);
  filter: hue-rotate(350deg) saturate(3) brightness(1.5) drop-shadow(0 0 20px #FFD700);
  box-shadow: 0 0 30px rgba(255, 215, 0, 0.6);
}

/* 🔥 NEW: PULSING NAV TABS */
.nav a {
  color: var(--text);
  text-decoration: none;
  font-weight: bold;
  font-size: 1.3rem;
  background: #FFD700;
  color: #2F4F2F;
  padding: 12px 20px;
  border-radius: 8px;
  transition: all 0.3s ease;
  margin: 0 5px;
  animation: navPulse 2s ease-in-out infinite;
}

.nav a:hover {
  background: #FFA500;
  transform: scale(1.05);
  color: white;
  box-shadow: 0 0 20px rgba(255, 165, 0, 0.8);
}

@keyframes navPulse {
  0%, 100% { box-shadow: 0 0 5px rgba(255, 215, 0, 0.5); }
  50% { box-shadow: 0 0 15px rgba(255, 215, 0, 0.8); }
}

/* Logo Animations */
@keyframes logoFadeIn {
  from { opacity: 0; transform: scale(0.8); }
  to { opacity: 1; transform: scale(1); }
}

@keyframes logoGlow {
  from { filter: hue-rotate(350deg) saturate(3) brightness(1.3); }
  to { filter: hue-rotate(350deg) saturate(3) brightness(1.4); }
}

/* 🔥 PARALLAX HERO */
.hero {
  height: 80vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  position: relative;
  overflow: hidden;
  animation: fadeIn 1s ease-in;
}

.hero-background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(rgba(47,79,47,0.7), rgba(47,79,47,0.3)), 
              url('https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80') center/cover;
  background-attachment: fixed; /* 🔥 PARALLAX */
  z-index: 1;
}

.hero-content {
  position: relative;
  z-index: 2;
  padding: 40px;
  background: rgba(47, 79, 47, 0.9);
  border-radius: 10px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
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
  transition: all 0.3s ease;
  box-shadow: 0 4px 15px rgba(255, 215, 0, 0.4);
}

.cta:hover {
  background: var(--accent);
  transform: scale(1.02); /* TINY scale = INSTANT click */
  box-shadow: 0 8px 25px rgba(255, 165, 0, 0.6);
}

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
  width: 600%;
}

.service-card {
  flex: 0 0 16.6667%;
  background: var(--background);
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
  box-sizing: border-box;
  transition: all 0.3s ease;
}

.service-card:hover {
  border: 2px solid var(--primary);
  transform: translateY(-5px);
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
  transition: all 0.3s ease;
  box-shadow: 0 4px 10px rgba(0,0,0,0.3);
}

.carousel-btn:hover {
  background: var(--accent);
  transform: translateY(-50%) scale(1.2);
}

.service-prev-btn { left: 10px; }
.service-next-btn { right: 10px; }

/* 🔥 3D PORTFOLIO TILT */
.portfolio {
  padding: 80px 20px;
  background: rgba(47, 79, 47, 0.85);
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

.carousel { position: relative; overflow: hidden; }

.carousel-track { display: flex; width: 2000%; }

.project {
  flex: 0 0 5%;
  display: flex;
  align-items: center;
  background: var(--background);
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
  overflow: hidden;
  transition: all 0.4s ease;
  transform-style: preserve-3d;
}

.project:hover {
  transform: translateY(-10px) rotateX(5deg) rotateY(5deg);
  box-shadow: 0 20px 40px rgba(0,0,0,0.4);
  border: 2px solid var(--primary);
}

.project-image {
  width: 50%;
  height: 300px;
  object-fit: cover;
  transition: all 0.3s ease;
}

.project:hover .project-image {
  transform: scale(1.05);
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
  transition: all 0.3s ease;
}

.project-link:hover {
  background: var(--accent);
  transform: scale(1.05);
}

.carousel-btn.prev-btn {
  left: 10px;
  opacity: 0;
  pointer-events: none;
  transition: all 0.3s ease;
}

.carousel-btn.next-btn {
  right: 10px;
  opacity: 0;
  pointer-events: none;
  transition: all 0.3s ease;
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

/* Modal */
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
  transition: all 0.3s ease;
}

.modal-close:hover {
  color: var(--primary);
  transform: rotate(90deg);
}

/* 🔥 SIMPLIFIED CONTACT MODAL */
.contact-modal .modal-content {
  background: var(--text);
  padding: 40px;
  border-radius: 10px;
  text-align: center;
  border: 2px solid var(--secondary);
  animation: modalSlideIn 0.3s ease;
  max-width: 400px;
}

@keyframes modalSlideIn {
  from { transform: scale(0.8); opacity: 0; }
  to { transform: scale(1); opacity: 1; }
}

.contact-modal h2 {
  font-size: 2rem;
  margin-bottom: 20px;
  color: var(--background);
}

.contact-info {
  margin: 30px 0;
  text-align: left;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 15px;
  margin-bottom: 20px;
  padding: 15px;
  background: rgba(47, 79, 47, 0.1);
  border-radius: 8px;
  border-left: 4px solid var(--primary);
}

.contact-icon {
  font-size: 1.5rem;
  flex-shrink: 0;
}

.contact-item strong {
  color: var(--background);
  font-size: 0.9rem;
  display: block;
  margin-bottom: 5px;
}

.copyable {
  color: var(--secondary);
  font-size: 1.2rem;
  font-weight: bold;
  font-family: 'Courier New', monospace;
  background: rgba(255, 255, 255, 0.1);
  padding: 5px 8px;
  border-radius: 4px;
  cursor: text;
  user-select: all; /* Makes it SUPER easy to select/copy */
}

.copyable:hover {
  background: rgba(255, 215, 0, 0.1);
  border: 1px solid var(--primary);
}

.contact-note {
  font-size: 1rem;
  color: var(--background);
  margin-top: 20px;
  font-style: italic;
}

/* Contact Section */
.contact {
  padding: 80px 20px;
  background: rgba(47, 79, 47, 0.85);
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

.footer-logo {
  margin-top: 20px;
}

.footer-logo-img {
  max-height: 160px;
  width: auto;
  filter: hue-rotate(350deg) saturate(3) brightness(1.3);
  transition: all 0.3s ease;
  animation: logoGlow 2s ease-in-out infinite alternate;
}

.footer-logo-img:hover {
  transform: scale(1.05);
  filter: hue-rotate(350deg) saturate(3) brightness(1.5) drop-shadow(0 0 20px #FFD700);
}

/* Responsive */
@media (max-width: 768px) {
  .header-container { flex-direction: column; gap: 10px; }
  .nav-left, .nav-right { justify-content: center; gap: 10px; }
  .header-logo { max-height: 200px; }
  .nav a { font-size: 1rem; }
  .hero h1 { font-size: 2.5rem; }
  .hero p { font-size: 1.2rem; }
  .hero { height: 70vh; }
  .hero-background { background-attachment: scroll; } /* No parallax on mobile */
  .hero-content { padding: 20px; }
  .about h2, .portfolio h2, .contact h2 { font-size: 2rem; }
  .services-carousel { max-width: 100%; }
  .service-prev-btn { left: 5px; }
  .service-next-btn { right: 5px; }
  .project { flex-direction: column; }
  .project-image { width: 100%; height: 200px; }
  .project-content { width: 100%; padding: 20px; }
  .carousel-btn.prev-btn, .carousel-btn.next-btn { 
    left: 5px; right: 5px; opacity: 1; pointer-events: auto; 
  }
  .footer-logo-img { max-height: 120px; }
  .modal-content { max-width: 90vw; }
  .modal-close { top: -20px; right: -20px; font-size: 1.5rem; }
}
</style>
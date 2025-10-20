<!-- HomeView.vue - NO CAROUSELS, PERFECT GRIDS -->
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

    <!-- About/Services Section - SIMPLE 3-CARD GRID -->
    <section class="about" id="about">
      <div class="container">
        <h2>What We Build</h2>
        <p class="about-intro">We craft clean, user-friendly websites for businesses.</p>
        <div class="services-grid">
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
      </div>
    </section>

    <!-- Portfolio Section - SIMPLE RESPONSIVE GRID -->
    <section class="portfolio" id="portfolio">
      <div class="container">
        <h2>Our Work</h2>
        <p class="portfolio-intro">Click any project to see details.</p>
        <div class="portfolio-grid">
          <article class="project">
            <img :src="images.tylerFurniture" alt="Furniture Co." class="project-image" @error="handleImageError" />
            <div class="project-content">
              
              <button @click="openImageModal(images.tylerFurniture)" class="project-link">View Details</button>
            </div>
          </article>
          <article class="project">
            <img :src="images.cedarCreekDrywall" alt="Drywall" class="project-image" @error="handleImageError" />
            <div class="project-content">
              
              <button @click="openImageModal(images.cedarCreekDrywall)" class="project-link">View Details</button>
            </div>
          </article>
          <article class="project">
            <img :src="images.cedarCreekDrywall2" alt="Drywall 2" class="project-image" @error="handleImageError" />
            <div class="project-content">
              
              <button @click="openImageModal(images.cedarCreekDrywall2)" class="project-link">View Details</button>
            </div>
          </article>
          <article class="project">
            <img :src="images.martinezBrosIrrigation" alt="Irrigation" class="project-image" @error="handleImageError" />
            <div class="project-content">
              
              <button @click="openImageModal(images.martinezBrosIrrigation)" class="project-link">View Details</button>
            </div>
          </article>
          <article class="project">
            <img :src="images.martinezBrosIrrigation2" alt="Irrigation 2" class="project-image" @error="handleImageError" />
            <div class="project-content">
              
              <button @click="openImageModal(images.martinezBrosIrrigation2)" class="project-link">View Details</button>
            </div>
          </article>
          <article class="project">
            <img :src="images.lakeviewCoffee" alt="Coffee Co." class="project-image" @error="handleImageError" />
            <div class="project-content">
              
              <button @click="openImageModal(images.lakeviewCoffee)" class="project-link">View Details</button>
            </div>
          </article>
          <article class="project">
            <img :src="images.lakeviewCoffee2" alt="Coffee Co. 2" class="project-image" @error="handleImageError" />
            <div class="project-content">
              
              <button @click="openImageModal(images.lakeviewCoffee2)" class="project-link">View Details</button>
            </div>
          </article>
          <article class="project">
            <img :src="images.lakeviewCoffee3" alt="Coffee Co. 3" class="project-image" @error="handleImageError" />
            <div class="project-content">
              
              <button @click="openImageModal(images.lakeviewCoffee3)" class="project-link">View Details</button>
            </div>
          </article>
          <article class="project">
            <img :src="images.eastTexasTavern" alt="Tavern" class="project-image" @error="handleImageError" />
            <div class="project-content">
              
              <button @click="openImageModal(images.eastTexasTavern)" class="project-link">View Details</button>
            </div>
          </article>
          <article class="project">
            <img :src="images.eastTexasTavern2" alt="Tavern 2" class="project-image" @error="handleImageError" />
            <div class="project-content">
              
              <button @click="openImageModal(images.eastTexasTavern2)" class="project-link">View Details</button>
            </div>
          </article>
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
        event.target.src = 'https://placehold.co/300x200/2F4F2F/F5F5DC?text=Project+Soon&font=montserrat';
      }
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
  }
};
</script>

<style scoped>
:root {
  --primary: #FFD700;
  --accent: #FFA500;
  --secondary: #2F4F2F;
  --background: #2F4F2F;
  --text: #F5F5DC;
}

.home {
  scroll-behavior: smooth;
  font-family: 'Montserrat', sans-serif;
  color: var(--text);
}

/* Header */
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

.logo-link { display: inline-block; text-decoration: none; }

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

.nav a {
  color: #2F4F2F;
  text-decoration: none;
  font-weight: bold;
  font-size: 1.3rem;
  background: #FFD700;
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

@keyframes logoFadeIn { from { opacity: 0; transform: scale(0.8); } to { opacity: 1; transform: scale(1); } }
@keyframes logoGlow { from { filter: hue-rotate(350deg) saturate(3) brightness(1.3); } to { filter: hue-rotate(350deg) saturate(3) brightness(1.4); } }

/* Hero */
.hero {
  height: 80vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.hero-background {
  position: absolute;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: linear-gradient(rgba(47,79,47,0.7), rgba(47,79,47,0.3)), 
              url('https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80') center/cover;
  background-attachment: fixed;
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

.hero p { font-size: 1.5rem; margin-bottom: 30px; color: var(--text); }

.cta {
  padding: 12px 24px;
  background: var(--primary);
  color: var(--text);
  border: none;
  border-radius: 5px;
  font-weight: bold;
  cursor: pointer;
  transition: all 0.3s ease;
  box-shadow: 0 4px 15px rgba(255, 215, 0, 0.4);
}

.cta:hover {
  background: var(--accent);
  transform: scale(1.02);
  box-shadow: 0 8px 25px rgba(255, 165, 0, 0.6);
}

/* SERVICES GRID - SIMPLE & PERFECT */
.about {
  padding: 80px 20px;
  background: var(--text);
}

.about h2 {
  font-size: 2.5rem;
  margin-bottom: 20px;
  color: var(--background);
  text-align: center;
  text-transform: uppercase;
}

.about-intro {
  font-size: 1.2rem;
  color: var(--background);
  margin-bottom: 40px;
  text-align: center;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  max-width: 1000px;
  margin: 0 auto;
}

.service-card {
  background: var(--background);
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
  transition: all 0.3s ease;
  text-align: center;
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

.service-card p { font-size: 1rem; color: var(--text); }

/* PORTFOLIO GRID - SIMPLE & PERFECT */
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

.portfolio-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  max-width: 1200px;
  margin: 0 auto;
}

.project {
  background: var(--background);
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
  overflow: hidden;
  transition: all 0.4s ease;
}

.project:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0,0,0,0.4);
  border: 2px solid var(--primary);
}

.project-image {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.project-content {
  padding: 20px;
  text-align: center;
}

.project h3 {
  font-size: 1.5rem;
  margin-bottom: 10px;
  color: var(--text);
}

.project-link {
  padding: 8px 16px;
  background: var(--primary);
  color: var(--text);
  border: none;
  border-radius: 5px;
  font-weight: bold;
  cursor: pointer;
  transition: all 0.3s ease;
}

.project-link:hover {
  background: var(--accent);
  transform: scale(1.05);
}

/* Modal */
.modal {
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
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
  top: 10px; right: 10px;
  font-size: 2rem;
  color: var(--secondary);
  cursor: pointer;
  transition: all 0.3s ease;
  z-index: 1001;
}

.modal-close:hover {
  color: var(--primary);
  transform: rotate(90deg);
}

/* Contact Modal */
.contact-modal .modal-content {
  background: var(--text);
  padding: 40px;
  border-radius: 10px;
  text-align: center;
  border: 2px solid var(--secondary);
  max-width: 400px;
}

.contact-modal h2 {
  font-size: 2rem;
  margin-bottom: 20px;
  color: var(--background);
}

.contact-info { margin: 30px 0; text-align: left; }

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

.contact-icon { font-size: 1.5rem; flex-shrink: 0; }

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
  user-select: all;
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
  text-align: center;
  text-transform: uppercase;
}

.contact p {
  font-size: 1.2rem;
  margin-bottom: 30px;
  color: var(--text);
  text-align: center;
}

.footer-logo { margin-top: 20px; text-align: center; }

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

/* MOBILE */
@media (max-width: 768px) {
  .header-container { flex-direction: column; gap: 10px; }
  .nav-left, .nav-right { justify-content: center; gap: 10px; }
  .header-logo { max-height: 200px; }
  .nav a { font-size: 1rem; }
  .hero h1 { font-size: 2.5rem; }
  .hero p { font-size: 1.2rem; }
  .hero { height: 70vh; }
  .hero-background { background-attachment: scroll; }
  .hero-content { padding: 20px; }
  .about h2, .portfolio h2, .contact h2 { font-size: 2rem; }
  .services-grid, .portfolio-grid { grid-template-columns: 1fr; gap: 15px; }
  .footer-logo-img { max-height: 120px; }
  .modal-content { max-width: 95vw; }
  .contact-modal .modal-content { max-width: 95vw; padding: 20px; margin: 10px; }
}
</style>
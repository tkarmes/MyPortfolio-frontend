<template>
  <div class="home">
    <!-- Hero Section -->
    <section class="hero">
      <div class="hero-split">
        <div class="hero-image"></div>
        <div class="hero-content">
          <h1>You Want It. I Build It.</h1>
          <p>Custom, responsive websites tailored for your business—built to grow in Tyler, TX.</p>
          <button @click="openContactModal" class="cta">Get a Free Quote</button>
        </div>
      </div>
    </section>

    <!-- About/Services Section -->
    <section class="about">
      <div class="container">
        <h2>What I Build</h2>
        <p class="about-intro">I craft clean, user-friendly websites for local businesses in Tyler and Cedar Creek Lake using Vue.js, JavaScript, and CSS.</p>
        <div class="services-carousel">
          <div class="services-track">
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
              <p>Optimized to rank higher and attract local clients.</p>
            </div>
          </div>
          <button class="carousel-btn service-prev-btn">←</button>
          <button class="carousel-btn service-next-btn">→</button>
        </div>
      </div>
    </section>

    <!-- Portfolio Section (Unchanged) -->
    <section class="portfolio">
      <div class="container">
        <h2>My Work</h2>
        <p class="portfolio-intro">Click the arrows to explore my business websites.</p>
        <div class="carousel">
          <div class="carousel-track">
            <article class="project">
              <img :src="images.tylerFurniture" alt="Tyler Furniture Co. Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Tyler Furniture Co.</h3>
                <p>A bold, responsive website for a Tyler, TX furniture store, featuring a modern hero, product grid, and sticky navigation for a premium user experience.</p>
                <p class="tech">Built with: HTML, CSS, JavaScript</p>
                <button @click="openImageModal(images.tylerFurniture)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.cedarCreekDrywall" alt="Cedar Creek Drywall Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Cedar Creek Drywall</h3>
                <p>A rugged, responsive site for a sheetrock contractor at Cedar Creek Lake, with fixed nav tabs, a drywall texture background, and real construction images.</p>
                <p class="tech">Built with: HTML, CSS, JavaScript</p>
                <button @click="openImageModal(images.cedarCreekDrywall)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.cedarCreekDrywall2" alt="Cedar Creek Drywall Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Cedar Creek Drywall</h3>
                <p>A fresh take on the sheetrock contractor site for Cedar Creek Lake, with a unique layout and enhanced visuals for local lakefront clients.</p>
                <p class="tech">Built with: HTML, CSS, JavaScript</p>
                <button @click="openImageModal(images.cedarCreekDrywall2)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.martinezBrosIrrigation" alt="Martinez Bros. Irrigation Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Martinez Bros. Irrigation</h3>
                <p>A responsive website for an East Texas irrigation company, featuring a fixed top navigation, lush lawn imagery, and a clean service grid for showcasing sprinkler and lawn care services.</p>
                <p class="tech">Built with: HTML, CSS, JavaScript</p>
                <button @click="openImageModal(images.martinezBrosIrrigation)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.martinezBrosIrrigation2" alt="Martinez Bros. Irrigation Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Martinez Bros. Irrigation</h3>
                <p>A unique take on the irrigation site with a bottom navigation bar, circular service cards, and a diagonal section tilt, showcasing a modern, dynamic layout for East Texas clients.</p>
                <p class="tech">Built with: HTML, CSS, JavaScript</p>
                <button @click="openImageModal(images.martinezBrosIrrigation2)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.lakeviewCoffee" alt="Lakeview Coffee Co. Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Lakeview Coffee Co.</h3>
                <p>A vibrant website for a Tyler, TX coffee shop, featuring a full-screen overlay menu with animated links, a split-screen hero with a large cozy coffee shop image, and a carousel slider for the menu.</p>
                <p class="tech">Built with: HTML, CSS, JavaScript</p>
                <button @click="openImageModal(images.lakeviewCoffee)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.lakeviewCoffee2" alt="Lakeview Coffee Co. Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Lakeview Coffee Co.</h3>
                <p>A dynamic take on the Tyler, TX coffee shop site, emphasizing the split-screen hero with right-aligned text and a carousel showcasing artisanal coffee and pastries.</p>
                <p class="tech">Built with: HTML, CSS, JavaScript</p>
                <button @click="openImageModal(images.lakeviewCoffee2)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.lakeviewCoffee3" alt="Lakeview Coffee Co. Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>Lakeview Coffee Co.</h3>
                <p>A fresh iteration of the coffee shop website, highlighting a fixed contact bar and a cozy aesthetic with a prominent background image for Tyler, TX clients.</p>
                <p class="tech">Built with: HTML, CSS, JavaScript</p>
                <button @click="openImageModal(images.lakeviewCoffee3)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.eastTexasTavern" alt="East Texas Tavern Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>East Texas Tavern</h3>
                <p>A modern website for a Tyler, TX bar, featuring a parallax scrolling hero, sticky navigation, tabbed menu for drinks and events, and a fixed social media footer.</p>
                <p class="tech">Built with: HTML, CSS, JavaScript</p>
                <button @click="openImageModal(images.eastTexasTavern)" class="project-link">View Details</button>
              </div>
            </article>
            <article class="project">
              <img :src="images.eastTexasTavern2" alt="East Texas Tavern Website Mockup" class="project-image" @error="handleImageError" />
              <div class="project-content">
                <h3>East Texas Tavern</h3>
                <p>A vibrant take on the Tyler, TX bar website, showcasing a scrolling marquee for live music events in the tabbed menu, paired with a gritty, rustic aesthetic.</p>
                <p class="tech">Built with: HTML, CSS, JavaScript</p>
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
      event.target.src = 'https://placehold.co/600x300/cccccc/333333?text=Project+Coming+Soon&font=montserrat';
    },
    initCarousel() {
      const track = document.querySelector('.carousel-track');
      const items = document.querySelectorAll('.project');
      const prevBtn = document.querySelector('.prev-btn');
      const nextBtn = document.querySelector('.next-btn');
      let currentIndex = 0;

      function updateCarousel() {
        track.style.transform = `translateX(-${currentIndex * 100}%)`;
      }

      nextBtn.addEventListener('click', () => {
        currentIndex = (currentIndex + 1) % items.length;
        updateCarousel();
      });

      prevBtn.addEventListener('click', () => {
        currentIndex = (currentIndex - 1 + items.length) % items.length;
        updateCarousel();
      });

      this.$nextTick(() => {
        updateCarousel();
      });
    },
    initServicesCarousel() {
      const track = document.querySelector('.services-track');
      const items = document.querySelectorAll('.service-card');
      const prevBtn = document.querySelector('.service-prev-btn');
      const nextBtn = document.querySelector('.service-next-btn');
      let currentIndex = 0;

      function updateCarousel() {
        track.style.transform = `translateX(-${currentIndex * 100}%)`;
      }

      nextBtn.addEventListener('click', () => {
        currentIndex = (currentIndex + 1) % items.length;
        updateCarousel();
      });

      prevBtn.addEventListener('click', () => {
        currentIndex = (currentIndex - 1 + items.length) % items.length;
        updateCarousel();
      });

      this.$nextTick(() => {
        updateCarousel();
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
    window.addEventListener('scroll', () => {
      const hero = document.querySelector('.hero-image');
      if (hero) {
        const scrollPosition = window.scrollY;
        hero.style.transform = `translateY(${scrollPosition * 0.3}px)`; // Parallax effect
      }
    });
  },
};
</script>

<style scoped>
.home {
  scroll-behavior: smooth;
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Hero Section */
.hero {
  height: 100vh;
  display: flex;
  align-items: center;
}
.hero-split {
  display: flex;
  width: 100%;
  height: 100%;
}
.hero-image {
  width: 60%;
  background: url('https://images.unsplash.com/photo-1516321310766-66f1ce1b41c2?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80') no-repeat center/cover;
  transition: transform 0.3s ease;
}
.hero-content {
  width: 40%;
  background: #3c2f2f; /* Dark wood brown from East Texas Tavern */
  color: #fff;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 40px;
}
.hero h1 {
  font-size: 3rem;
  margin-bottom: 20px;
}
.hero p {
  font-size: 1.2rem;
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

/* About Section */
.about {
  padding: 80px 20px;
  background: #fff;
  text-align: center;
}
.about h2 {
  font-size: 2.5rem;
  margin-bottom: 20px;
  color: #333;
}
.about-intro {
  font-size: 1.2rem;
  color: #555;
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
  transition: transform 0.7s ease; /* Slower transition for readability */
}
.service-card {
  flex: 0 0 100%; /* Full width per card */
  background: #f9f9f9;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  box-sizing: border-box;
}
.service-card h3 {
  font-size: 1.5rem;
  margin-bottom: 10px;
  color: #333;
}
.service-card p {
  font-size: 1rem;
  color: #666;
}
.carousel-btn {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(0, 123, 255, 0.7);
  color: #fff;
  border: none;
  padding: 10px;
  cursor: pointer;
  font-size: 1.5rem;
  border-radius: 50%;
}
.service-prev-btn {
  left: 10px;
}
.service-next-btn {
  right: 10px;
}

/* Portfolio Section (Unchanged) */
.portfolio {
  padding: 80px 20px;
  background: #f9f9f9;
}
.portfolio h2 {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 10px;
}
.portfolio-intro {
  text-align: center;
  font-size: 1rem;
  color: #555;
  margin-bottom: 40px;
}
.carousel {
  position: relative;
  overflow: hidden;
}
.carousel-track {
  display: flex;
  transition: transform 0.5s ease;
}
.project {
  flex: 0 0 100%;
  display: flex;
  align-items: center;
  background: #fff;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  overflow: hidden;
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
  display: inline-block;
  padding: 8px 16px;
  background: #007bff;
  color: white;
  text-decoration: none;
  border-radius: 5px;
  font-weight: bold;
  cursor: pointer;
  transition: background 0.3s;
}
.project-link:hover {
  background: #0056b3;
}
.carousel-btn.prev-btn {
  left: 10px;
}
.carousel-btn.next-btn {
  right: 10px;
}

/* Modal (Image and Contact) */
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.8);
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
}
.modal-close {
  position: absolute;
  top: -30px;
  right: -30px;
  font-size: 2rem;
  color: #fff;
  cursor: pointer;
}
.contact-modal .modal-content {
  background: #fff;
  padding: 40px;
  border-radius: 10px;
  text-align: center;
}
.contact-modal h2 {
  font-size: 2rem;
  margin-bottom: 20px;
}
.contact-modal p {
  font-size: 1.1rem;
  color: #555;
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
  border: 1px solid #ccc;
  border-radius: 5px;
  font-size: 1rem;
}
.contact-form textarea {
  height: 100px;
  resize: none;
}
.email-copy {
  margin-top: 10px;
}

/* Contact Section */
.contact {
  padding: 80px 20px;
  background: #3c2f2f;
  color: #fff;
  text-align: center;
}
.contact h2 {
  font-size: 2.5rem;
  margin-bottom: 20px;
}
.contact p {
  font-size: 1.2rem;
  margin-bottom: 30px;
}

/* Responsive */
@media (max-width: 768px) {
  .hero-split {
    flex-direction: column;
  }
  .hero-image {
    width: 100%;
    height: 50vh;
  }
  .hero-content {
    width: 100%;
    padding: 20px;
  }
  .hero h1 {
    font-size: 2rem;
  }
  .hero p {
    font-size: 1rem;
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
    flex: 0 0 100%;
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
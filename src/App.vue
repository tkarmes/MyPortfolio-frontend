<template>
  <div
    id="app"
    :style="{
      backgroundImage: `url(${woodTexture})`,
      backgroundRepeat: 'no-repeat',
      backgroundPosition: 'center center',
      backgroundAttachment: 'fixed',
      backgroundSize: 'cover',
      backgroundColor: 'var(--background)',
      minHeight: '100vh',
      display: 'flex',
      flexDirection: 'column'
    }"
  >
    <!-- All page content goes here via router -->
    <router-view />

    <!-- Site-Wide Footer -->
    <footer class="site-footer">
      <div class="footer-container">
        <p>&copy; {{ new Date().getFullYear() }} Web Rousers. All rights reserved.</p>
        <p>Made with <span class="heart">love</span> & Vue.js</p>
      </div>
    </footer>
  </div>
</template>

<script>
import woodTexture from '@/assets/wood-texture.jpg';

export default {
  data() {
    return {
      woodTexture,
    };
  },
};
</script>

<style>
/* Global CSS Variables */
:root {
  --background: #2F4F2F; /* Dark olive green */
  --text: #F5F5DC;       /* Beige */
  --primary: #6B8E23;    /* Olive drab */
  --secondary: #DAA520;  /* Goldenrod */
  --accent: #556B2F;     /* Dark olive */
}

html, body, #app {
  font-family: 'Montserrat', sans-serif;
  text-align: center;
  color: var(--text);
  margin: 0;
  padding: 0;
  height: 100%;
}

/* Footer Styling */
.site-footer {
  background: rgba(47, 79, 47, 0.95);
  color: var(--text);
  padding: 2rem 1rem;
  text-align: center;
  font-size: 0.9rem;
  border-top: 3px solid var(--secondary);
  margin-top: auto; /* Pushes footer to bottom */
  backdrop-filter: blur(4px);
}

.footer-container {
  max-width: 1200px;
  margin: 0 auto;
}

.site-footer p {
  margin: 0.5rem 0;
  font-weight: 300;
}

.heart {
  color: #FFD700;
  font-weight: bold;
}

/* Responsive */
@media (max-width: 768px) {
  .site-footer {
    padding: 1.5rem 1rem;
    font-size: 0.8rem;
  }
}
</style>
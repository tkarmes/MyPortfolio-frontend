<template>
  <div
    id="app"
    :style="{
      backgroundImage: `url(${woodTexture})`,
      backgroundRepeat: 'no-repeat',
      backgroundPosition: 'center center',
      backgroundAttachment: 'fixed',
      backgroundSize: 'cover',
      backgroundColor: 'var(--background)', // Fallback if image fails
      minHeight: '100vh'
    }"
  >
    <router-view />
  </div>
</template>

<script>
import woodTexture from '@/assets/wood-texture.jpg'; // Import the image from src/assets

export default {
  data() {
    return {
      woodTexture, // Reference the imported image
    };
  },
};
</script>

<style>
/* Global CSS Variables */
:root {
  --background: #2F4F2F; /* Dark olive green for an earthy base */
  --text: #F5F5DC; /* Beige for a natural text color */
  --primary: #6B8E23; /* Olive drab for highlights */
  --secondary: #DAA520; /* Goldenrod for a warm, forest glow */
  --accent: #556B2F; /* Dark olive green for depth */
}

html, body, #app {
  font-family: 'Montserrat', sans-serif;
  text-align: center;
  color: var(--text);
  margin: 0;
  padding: 0;
}
</style>
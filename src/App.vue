<template>
  <div id="app">
    <router-view />
  </div>
</template>

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
  background: var(--background);
  color: var(--text);
  min-height: 100vh;
  margin: 0;
  padding: 0;
}
</style>
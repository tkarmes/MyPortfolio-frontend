<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style>
/* Global CSS Variables */
:root {
  --background: #1A1A1A; /* Dark gray */
  --text: #FFFFFF; /* White */
  --primary: #0A84FF; /* Light blue */
  --secondary: #FFD700; /* Gold yellow */
  --accent: #0052D4; /* Darker blue for hover */
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
<template>
  <div class="contact">
    <h2>Contact Me</h2>
    <p>Reach out to discuss your website or app project!</p>
    <button @click="copyEmail" class="cta">Copy Email: armes@webrousers.com</button>
    <p>Or manually copy: <strong>armes@webrousers.com</strong></p>
  </div>
</template>

<script>
export default {
  methods: {
    async copyEmail() {
      const email = 'armes@webrousers.com';
      try {
        await navigator.clipboard.writeText(email);
        alert('Email copied to clipboard! Paste it into your email client.');
        console.log('Copy button clicked at ' + new Date().toLocaleTimeString());
      } catch (err) {
        console.error('Failed to copy: ', err);
        alert('Copy failed—please select and copy the email manually.');
      }
    },
  },
};
</script>

<style scoped>
.contact {
  max-width: 600px;
  margin: 50px auto;
  text-align: center;
}
.contact h2 {
  font-size: 2rem;
  margin-bottom: 20px;
}
.contact p {
  font-size: 1.2rem;
  color: #555;
  margin-bottom: 20px;
}
.cta {
  display: inline-block;
  padding: 12px 24px;
  background: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  font-weight: bold;
  cursor: pointer;
  transition: background 0.3s;
}
.cta:hover {
  background: #0056b3;
}
</style>
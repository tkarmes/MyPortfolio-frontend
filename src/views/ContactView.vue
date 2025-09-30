<template>
  <div class="contact">
    <h2>Contact Me</h2>
    <form @submit.prevent="submitForm">
      <input v-model="form.name" type="text" placeholder="Name" required />
      <input v-model="form.email" type="email" placeholder="Email" required />
      <textarea v-model="form.message" placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
      <p v-if="success">Message sent successfully!</p>
      <p v-if="error" class="error">Error: {{ error }}</p>
    </form>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: '',
      },
      success: false,
      error: null,
    };
  },
  methods: {
    async submitForm() {
      try {
        await axios.post('http://localhost:8080/api/contact', this.form);
        this.success = true;
        this.error = null;
        this.form = { name: '', email: '', message: '' };
      } catch (err) {
        this.error = err.message;
        this.success = false;
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
input,
textarea {
  display: block;
  width: 100%;
  margin: 10px 0;
  padding: 10px;
}
textarea {
  height: 100px;
}
button {
  padding: 10px 20px;
  background: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
}
.error {
  color: red;
}
</style>
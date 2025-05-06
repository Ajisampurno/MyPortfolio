<script setup>
import { ref } from 'vue'
import Navbar from '@/components/Navbar.vue'

const name = ref('')
const email = ref('')
const message = ref('')

const sendMessage = () => {
  const phone = '+6283117764077'
  const text = `Name: ${name.value}\nEmail: ${email.value}\nMessage: ${message.value}`
  const url = `https://wa.me/${phone}?text=${encodeURIComponent(text)}`
  window.open(url, '_blank')
}
</script>

<template>
  <div>
    <!-- Navbar with fixed position -->
    <Navbar />
    <div class="main-container">
      <div class="row">
        <div class="col-md-6">
          <div class="contact-content">
            <h1>Contact Information</h1>
            <p>If you have any questions, feel free to reach out:</p>
            <ul>
              <li>
                Email: <a href="mailto:aji97.jobs@gmail.commence">aji97.jobs@gmail.commence</a>
              </li>
              <li>Phone: +62 831 1776 4077</li>
              <li>
                LinkedIn:
                <a href="https://www.linkedin.com/in/aji-sampurno97/" target="_blank"
                  >Aji Sampurno</a
                >
              </li>
              <li>
                GitHub: <a href="https://github.com/Ajisampurno" target="_blank">ajisampurno</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="col-md-6">
          <div class="contact-content">
            <h2>Send a Message</h2>
            <form @submit.prevent="sendMessage">
              <div class="mb-3">
                <label for="name" class="form-label">Name</label>
                <input type="text" id="name" v-model="name" class="form-control" required />
              </div>
              <div class="mb-3">
                <label for="email" class="form-label">Email</label>
                <input type="email" id="email" v-model="email" class="form-control" required />
              </div>
              <div class="mb-3">
                <label for="message" class="form-label">Message</label>
                <textarea
                  id="message"
                  v-model="message"
                  class="form-control"
                  rows="5"
                  required
                ></textarea>
              </div>
              <button type="submit" class="btn btn-primary shadow-button">Send to WhatsApp</button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.main-container {
  display: flex;
  justify-content: center;
  padding-top: 100px; /* Adjust padding to prevent overlap with navbar */
  padding-bottom: 30px;
  background: url('../assets/backgound/bg-cover.png') no-repeat center center fixed;
  background-size: cover;
  color: #f8f9fa;
}

.contact-content {
  background-color: rgba(0, 0, 0, 0.7);
  padding: 20px 30px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
  max-width: 600px;
}

h1,
h2 {
  margin-bottom: 20px;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
}

p,
li,
a {
  color: #f8f9fa;
}

ul {
  list-style: none;
  padding: 0;
}

li {
  margin: 10px 0;
}

a {
  color: #1e90ff;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

form {
  margin-top: 20px;
}

.form-label {
  color: #f8f9fa;
}

.form-control {
  background-color: #2c2c2c;
  color: #f8f9fa;
  border: 1px solid #555;
}

.form-control:focus {
  background-color: #2c2c2c;
  color: #f8f9fa;
  border-color: #1e90ff;
  box-shadow: 0 0 5px rgba(30, 144, 255, 0.5);
}

.btn-primary {
  background-color: #1e90ff;
  border-color: #1e90ff;
}

.btn-primary:hover {
  background-color: #1c86ee;
  border-color: #1c86ee;
}

/* Fixed Navbar Styles */
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000; /* Ensures navbar stays on top */
}

/* Adjust main padding-top to make space for the fixed navbar */
main {
  padding-top: 80px; /* Adjust according to navbar height */
}
</style>

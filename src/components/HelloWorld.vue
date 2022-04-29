<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)
</script>

<template>
 <nav>
  <img src="images/logo.svg" alt="logo">
  <ul>
  Features
  Company
  Careers
  About

  Login
  Register
</ul>
</nav>
<main>
  <h1>Make remote work</h1>

  <p>Get your team in sync, no matter your location. Streamline processes, 
  create team rituals, and watch productivity soar.</p>

  <button>Learn more</button>
  <img src="images/client-databiz.svg" alt="data biz">
  <img src="images/client-audiophile.svg" alt="audio phile">
  <img src="images/client-meet.svg" alt="meet">
  <img src="images/client-maker.svg" alt="maker">
  <picture>
    <source media="(min-width: 45em)" srcset="images/image-hero-desktop.png">
  <img src="images/image-hero-mobile.png" alt="Remote work">
</picture>
</main>
</template>

<style scoped>
a {
  color: #42b983;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}
</style>

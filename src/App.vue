<template>
  <div class="app">
    <Header />
    <Hero />
    <Expertise />
    <Team />
    <Contact />
    <Footer />
  </div>
</template>

<script setup>
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import Expertise from './components/Expertise.vue'
import Team from './components/Team.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Inter', sans-serif;
  color: #1a1a1a;
  overflow-x: hidden;
}

.app {
  min-height: 100vh;
}
</style>


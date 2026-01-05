<template>
  <header class="header" :class="{ scrolled: isScrolled }">
    <div class="container">
      <div class="logo">
        <h1>Lexington<span>Partners</span></h1>
      </div>
      
      <nav class="nav" :class="{ active: mobileMenuOpen }">
        <a href="#home" @click="scrollTo('home')">Home</a>
        <a href="#services" @click="scrollTo('services')">Services</a>
        <a href="#about" @click="scrollTo('about')">About</a>
        <a href="#team" @click="scrollTo('team')">Team</a>
        <a href="#contact" @click="scrollTo('contact')">Contact</a>
      </nav>
      
      <button class="mobile-toggle" @click="mobileMenuOpen = !mobileMenuOpen">
        <span></span>
        <span></span>
        <span></span>
      </button>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)
const mobileMenuOpen = ref(false)

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50
}

const scrollTo = (section) => {
  mobileMenuOpen.value = false
  const element = document.getElementById(section)
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  padding: 1.5rem 0;
  transition: all 0.3s ease;
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(10px);
}

.header.scrolled {
  padding: 1rem 0;
  background: rgba(255, 255, 255, 0.98);
  box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo h1 {
  font-family: 'Playfair Display', serif;
  font-size: 1.5rem;
  font-weight: 600;
  color: #fff;
  transition: color 0.3s ease;
}

.header.scrolled .logo h1 {
  color: #1a1a1a;
}

.logo span {
  display: block;
  font-size: 0.9rem;
  font-weight: 300;
  letter-spacing: 2px;
}

.nav {
  display: flex;
  gap: 2.5rem;
}

.nav a {
  color: #fff;
  text-decoration: none;
  font-weight: 500;
  font-size: 0.95rem;
  transition: all 0.3s ease;
  position: relative;
}

.header.scrolled .nav a {
  color: #1a1a1a;
}

.nav a::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 2px;
  background: #c9a961;
  transition: width 0.3s ease;
}

.nav a:hover::after {
  width: 100%;
}

.mobile-toggle {
  display: none;
  flex-direction: column;
  gap: 5px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 5px;
}

.mobile-toggle span {
  width: 25px;
  height: 2px;
  background: #fff;
  transition: all 0.3s ease;
}

.header.scrolled .mobile-toggle span {
  background: #1a1a1a;
}

@media (max-width: 768px) {
  .nav {
    position: fixed;
    top: 0;
    right: -100%;
    width: 70%;
    height: 100vh;
    background: rgba(26, 26, 26, 0.98);
    flex-direction: column;
    padding: 5rem 2rem;
    transition: right 0.3s ease;
  }
  
  .nav.active {
    right: 0;
  }
  
  .nav a {
    color: #fff !important;
    font-size: 1.2rem;
  }
  
  .mobile-toggle {
    display: flex;
    z-index: 1001;
  }
}
</style>


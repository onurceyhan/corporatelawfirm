<template>
  <section id="home" class="hero">
    <div class="hero-overlay"></div>
    <div class="decorative-lines">
      <div class="line line-1"></div>
      <div class="line line-2"></div>
    </div>
    
    <div class="hero-content">
      <h1 class="hero-title">
        <span class="title-line">Trusted Legal</span>
        <span class="title-line">Advisors</span>
      </h1>
      <p class="hero-subtitle">Excellence in legal representation since 1995</p>
      <button class="cta-button" @click="scrollToContact">Book Consultation</button>
    </div>
    
    <div class="scroll-indicator">
      <span></span>
    </div>
  </section>
</template>

<script setup>
const scrollToContact = () => {
  const contact = document.getElementById('contact')
  if (contact) {
    contact.scrollIntoView({ behavior: 'smooth' })
  }
}
</script>

<style scoped>
.hero {
  position: relative;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, #2c3e50 0%, #34495e 100%);
  background-image: url('https://images.unsplash.com/photo-1589829545856-d10d557cf95f?w=1600&q=80');
  background-size: cover;
  background-position: center;
  overflow: hidden;
}

.hero-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, rgba(26, 26, 26, 0.85) 0%, rgba(44, 62, 80, 0.75) 100%);
}

.decorative-lines {
  position: absolute;
  inset: 0;
  overflow: hidden;
}

.line {
  position: absolute;
  width: 1px;
  height: 400px;
  background: linear-gradient(to bottom, transparent, #c9a961, transparent);
  opacity: 0.3;
}

.line-1 {
  top: -100px;
  left: 15%;
  transform: rotate(25deg);
  animation: lineMove 8s ease-in-out infinite;
}

.line-2 {
  bottom: -100px;
  right: 15%;
  transform: rotate(25deg);
  animation: lineMove 8s ease-in-out infinite reverse;
}

@keyframes lineMove {
  0%, 100% { transform: translateY(0) rotate(25deg); }
  50% { transform: translateY(50px) rotate(25deg); }
}

.hero-content {
  position: relative;
  z-index: 10;
  text-align: center;
  color: #fff;
  max-width: 900px;
  padding: 0 2rem;
}

.hero-title {
  font-family: 'Playfair Display', serif;
  font-size: 5rem;
  font-weight: 700;
  line-height: 1.1;
  margin-bottom: 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.title-line {
  display: block;
  opacity: 0;
  transform: translateY(30px);
  animation: fadeInUp 1s ease forwards;
}

.title-line:nth-child(2) {
  animation-delay: 0.2s;
}

@keyframes fadeInUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.hero-subtitle {
  font-size: 1.25rem;
  font-weight: 300;
  margin-bottom: 3rem;
  opacity: 0;
  animation: fadeIn 1s ease 0.6s forwards;
  letter-spacing: 1px;
}

@keyframes fadeIn {
  to { opacity: 1; }
}

.cta-button {
  background: #c9a961;
  color: #fff;
  border: none;
  padding: 1.2rem 3rem;
  font-size: 1rem;
  font-weight: 600;
  letter-spacing: 1px;
  cursor: pointer;
  transition: all 0.3s ease;
  opacity: 0;
  animation: fadeIn 1s ease 0.8s forwards;
  text-transform: uppercase;
}

.cta-button:hover {
  background: #b8954d;
  transform: translateY(-3px);
  box-shadow: 0 10px 30px rgba(201, 169, 97, 0.4);
}

.scroll-indicator {
  position: absolute;
  bottom: 3rem;
  left: 50%;
  transform: translateX(-50%);
  z-index: 10;
}

.scroll-indicator span {
  display: block;
  width: 1px;
  height: 60px;
  background: linear-gradient(to bottom, #c9a961, transparent);
  animation: scrollAnim 2s ease-in-out infinite;
}

@keyframes scrollAnim {
  0%, 100% { opacity: 0.3; height: 60px; }
  50% { opacity: 1; height: 80px; }
}

@media (max-width: 768px) {
  .hero-title {
    font-size: 3rem;
  }
  
  .hero-subtitle {
    font-size: 1rem;
  }
  
  .cta-button {
    padding: 1rem 2rem;
    font-size: 0.9rem;
  }
}
</style>


<template>
  <section id="services" class="expertise">
    <div class="container">
      <div class="section-header">
        <span class="section-label">OUR EXPERTISE</span>
        <h2 class="section-title">Legal Services</h2>
      </div>
      
      <div class="services-grid">
        <div 
          v-for="(service, index) in services" 
          :key="index" 
          class="service-card"
          :style="{ animationDelay: `${index * 0.1}s` }"
        >
          <div class="service-icon">
            <span v-html="service.icon"></span>
          </div>
          <h3 class="service-title">{{ service.title }}</h3>
          <p class="service-description">{{ service.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  {
    icon: '⚖️',
    title: 'Corporate Law',
    description: 'Comprehensive legal solutions for businesses, including mergers, acquisitions, and corporate governance matters.'
  },
  {
    icon: '🏛️',
    title: 'Litigation',
    description: 'Expert representation in civil and commercial disputes to protect your interests in court.'
  },
  {
    icon: '💡',
    title: 'Intellectual Property',
    description: 'Protecting your innovations, trademarks, and creative works with strategic IP management.'
  },
  {
    icon: '🏢',
    title: 'Real Estate Law',
    description: 'Complete legal support for property transactions, development projects, and real estate disputes.'
  },
  {
    icon: '👔',
    title: 'Employment Law',
    description: 'Advising on employment contracts, workplace disputes, and compliance with labor regulations.'
  },
  {
    icon: '📋',
    title: 'Contract Law',
    description: 'Drafting, reviewing, and negotiating contracts to protect your business interests.'
  }
]
</script>

<style scoped>
.expertise {
  padding: 8rem 0;
  background: #f8f9fa;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.section-header {
  text-align: center;
  margin-bottom: 5rem;
}

.section-label {
  display: inline-block;
  font-size: 0.85rem;
  font-weight: 600;
  letter-spacing: 3px;
  color: #c9a961;
  margin-bottom: 1rem;
}

.section-title {
  font-family: 'Playfair Display', serif;
  font-size: 3rem;
  font-weight: 700;
  color: #1a1a1a;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2.5rem;
}

.service-card {
  background: #fff;
  padding: 3rem 2rem;
  border-radius: 8px;
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
  opacity: 0;
  animation: fadeInUp 0.8s ease forwards;
}

.service-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: linear-gradient(90deg, #c9a961, #b8954d);
  transform: scaleX(0);
  transition: transform 0.3s ease;
  transform-origin: left;
}

.service-card:hover::before {
  transform: scaleX(1);
}

.service-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 50px rgba(0, 0, 0, 0.1);
}

.service-icon {
  font-size: 3rem;
  margin-bottom: 1.5rem;
}

.service-title {
  font-family: 'Playfair Display', serif;
  font-size: 1.5rem;
  font-weight: 600;
  color: #1a1a1a;
  margin-bottom: 1rem;
}

.service-description {
  color: #666;
  line-height: 1.8;
  font-size: 0.95rem;
}

@keyframes fadeInUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 768px) {
  .expertise {
    padding: 5rem 0;
  }
  
  .section-title {
    font-size: 2rem;
  }
  
  .services-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
}
</style>


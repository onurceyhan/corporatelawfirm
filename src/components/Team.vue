<template>
  <section id="team" class="team">
    <div class="container">
      <div class="section-header">
        <span class="section-label">OUR TEAM</span>
        <h2 class="section-title">Meet Our Attorneys</h2>
        <p class="section-subtitle">
          Experienced legal professionals dedicated to achieving the best outcomes for our clients
        </p>
      </div>
      
      <div class="team-grid">
        <div 
          v-for="(member, index) in team" 
          :key="index" 
          class="team-member"
          :style="{ animationDelay: `${index * 0.15}s` }"
        >
          <div class="member-image">
            <img :src="member.image" :alt="member.name" />
            <div class="member-overlay">
              <div class="social-links">
                <a href="#" aria-label="LinkedIn">
                  <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                    <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
                  </svg>
                </a>
              </div>
            </div>
          </div>
          <div class="member-info">
            <h3 class="member-name">{{ member.name }}</h3>
            <p class="member-title">{{ member.title }}</p>
            <p class="member-description">{{ member.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const team = [
  {
    name: 'Michael Anderson',
    title: 'Senior Partner',
    description: '25+ years of experience in corporate law and mergers & acquisitions',
    image: 'https://images.unsplash.com/photo-1556157382-97eda2d62296?w=400&q=80'
  },
  {
    name: 'Sarah Mitchell',
    title: 'Managing Partner',
    description: 'Specialized in intellectual property and technology law',
    image: 'https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?w=400&q=80'
  },
  {
    name: 'James Patterson',
    title: 'Partner',
    description: 'Expert litigator with a proven track record in commercial disputes',
    image: 'https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=400&q=80'
  },
  {
    name: 'Emily Chen',
    title: 'Partner',
    description: 'Focused on employment law and regulatory compliance',
    image: 'https://images.unsplash.com/photo-1580489944761-15a19d654956?w=400&q=80'
  }
]
</script>

<style scoped>
.team {
  padding: 8rem 0;
  background: #fff;
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
  margin-bottom: 1rem;
}

.section-subtitle {
  color: #666;
  font-size: 1.1rem;
  max-width: 600px;
  margin: 0 auto;
  line-height: 1.6;
}

.team-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 3rem;
}

.team-member {
  opacity: 0;
  animation: fadeInUp 0.8s ease forwards;
}

.member-image {
  position: relative;
  overflow: hidden;
  border-radius: 8px;
  margin-bottom: 1.5rem;
  aspect-ratio: 3/4;
}

.member-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
}

.member-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(to top, rgba(26, 26, 26, 0.9), transparent);
  display: flex;
  align-items: flex-end;
  justify-content: center;
  padding: 2rem;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.team-member:hover .member-image img {
  transform: scale(1.1);
}

.team-member:hover .member-overlay {
  opacity: 1;
}

.social-links {
  display: flex;
  gap: 1rem;
}

.social-links a {
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(255, 255, 255, 0.1);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 50%;
  color: #fff;
  transition: all 0.3s ease;
}

.social-links a:hover {
  background: #c9a961;
  border-color: #c9a961;
  transform: translateY(-3px);
}

.member-name {
  font-family: 'Playfair Display', serif;
  font-size: 1.5rem;
  font-weight: 600;
  color: #1a1a1a;
  margin-bottom: 0.5rem;
}

.member-title {
  color: #c9a961;
  font-weight: 600;
  margin-bottom: 1rem;
  text-transform: uppercase;
  font-size: 0.85rem;
  letter-spacing: 1px;
}

.member-description {
  color: #666;
  line-height: 1.6;
  font-size: 0.95rem;
}

@keyframes fadeInUp {
  to {
    opacity: 1;
  }
}

@media (max-width: 768px) {
  .team {
    padding: 5rem 0;
  }
  
  .section-title {
    font-size: 2rem;
  }
  
  .team-grid {
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
  }
}
</style>


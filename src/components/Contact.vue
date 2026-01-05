<template>
  <section id="contact" class="contact">
    <div class="container">
      <div class="contact-wrapper">
        <div class="contact-info">
          <div class="section-header">
            <span class="section-label">GET IN TOUCH</span>
            <h2 class="section-title">Schedule a Consultation</h2>
            <p class="section-subtitle">
              Contact us today for expert legal advice tailored to your needs
            </p>
          </div>
          
          <div class="info-items">
            <div class="info-item">
              <div class="info-icon">📍</div>
              <div class="info-content">
                <h4>Address</h4>
                <p>125 Business Ave, Suite 3721<br>New York, NY 10017</p>
              </div>
            </div>
            
            <div class="info-item">
              <div class="info-icon">📞</div>
              <div class="info-content">
                <h4>Phone</h4>
                <p>+1 (555) 123-4567</p>
              </div>
            </div>
            
            <div class="info-item">
              <div class="info-icon">✉️</div>
              <div class="info-content">
                <h4>Email</h4>
                <p>info@lexingtonlaw.com</p>
              </div>
            </div>
            
            <div class="info-item">
              <div class="info-icon">🕐</div>
              <div class="info-content">
                <h4>Office Hours</h4>
                <p>Monday - Friday: 9:00 AM - 6:00 PM<br>Saturday: 10:00 AM - 2:00 PM</p>
              </div>
            </div>
          </div>
        </div>
        
        <div class="contact-form-wrapper">
          <form @submit.prevent="handleSubmit" class="contact-form">
            <div class="form-group">
              <input 
                type="text" 
                v-model="form.name" 
                placeholder="Your Name" 
                required 
              />
            </div>
            
            <div class="form-group">
              <input 
                type="email" 
                v-model="form.email" 
                placeholder="Your Email" 
                required 
              />
            </div>
            
            <div class="form-group">
              <input 
                type="tel" 
                v-model="form.phone" 
                placeholder="Phone Number" 
              />
            </div>
            
            <div class="form-group">
              <select v-model="form.service" required>
                <option value="">Select Service</option>
                <option value="corporate">Corporate Law</option>
                <option value="litigation">Litigation</option>
                <option value="ip">Intellectual Property</option>
                <option value="realestate">Real Estate Law</option>
                <option value="employment">Employment Law</option>
                <option value="contract">Contract Law</option>
              </select>
            </div>
            
            <div class="form-group">
              <textarea 
                v-model="form.message" 
                placeholder="Tell us about your case" 
                rows="5"
                required
              ></textarea>
            </div>
            
            <button type="submit" class="submit-button">
              Send Message
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const form = ref({
  name: '',
  email: '',
  phone: '',
  service: '',
  message: ''
})

const handleSubmit = () => {
  alert('Thank you for your message! We will contact you shortly.')
  form.value = {
    name: '',
    email: '',
    phone: '',
    service: '',
    message: ''
  }
}
</script>

<style scoped>
.contact {
  padding: 8rem 0;
  background: linear-gradient(135deg, #2c3e50 0%, #34495e 100%);
  color: #fff;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.contact-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: start;
}

.section-header {
  margin-bottom: 3rem;
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
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 1rem;
}

.section-subtitle {
  color: rgba(255, 255, 255, 0.8);
  font-size: 1.05rem;
  line-height: 1.6;
}

.info-items {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.info-item {
  display: flex;
  gap: 1.5rem;
  align-items: flex-start;
}

.info-icon {
  font-size: 2rem;
  flex-shrink: 0;
}

.info-content h4 {
  font-weight: 600;
  margin-bottom: 0.5rem;
  font-size: 1.1rem;
}

.info-content p {
  color: rgba(255, 255, 255, 0.8);
  line-height: 1.6;
}

.contact-form-wrapper {
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(10px);
  padding: 3rem;
  border-radius: 12px;
  border: 1px solid rgba(255, 255, 255, 0.1);
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.form-group input,
.form-group select,
.form-group textarea {
  width: 100%;
  padding: 1rem 1.5rem;
  background: rgba(255, 255, 255, 0.1);
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-radius: 8px;
  color: #fff;
  font-size: 1rem;
  transition: all 0.3s ease;
  font-family: 'Inter', sans-serif;
}

.form-group input::placeholder,
.form-group textarea::placeholder {
  color: rgba(255, 255, 255, 0.5);
}

.form-group input:focus,
.form-group select:focus,
.form-group textarea:focus {
  outline: none;
  border-color: #c9a961;
  background: rgba(255, 255, 255, 0.15);
}

.form-group select {
  cursor: pointer;
}

.form-group select option {
  background: #2c3e50;
  color: #fff;
}

.submit-button {
  background: #c9a961;
  color: #fff;
  border: none;
  padding: 1.2rem 3rem;
  font-size: 1rem;
  font-weight: 600;
  letter-spacing: 1px;
  cursor: pointer;
  transition: all 0.3s ease;
  text-transform: uppercase;
  border-radius: 8px;
}

.submit-button:hover {
  background: #b8954d;
  transform: translateY(-2px);
  box-shadow: 0 10px 30px rgba(201, 169, 97, 0.3);
}

@media (max-width: 968px) {
  .contact-wrapper {
    grid-template-columns: 1fr;
    gap: 3rem;
  }
}

@media (max-width: 768px) {
  .contact {
    padding: 5rem 0;
  }
  
  .section-title {
    font-size: 2rem;
  }
  
  .contact-form-wrapper {
    padding: 2rem;
  }
}
</style>


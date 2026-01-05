# Corporate Law Firm Website

A modern, professional law firm website built with Vue 3 and Vite, featuring a sophisticated design with smooth animations and full responsive support.

[![Built with Vue 3](https://img.shields.io/badge/Vue-3.x-42b883?style=flat-square&logo=vue.js)](https://vuejs.org/)
[![Powered by Vite](https://img.shields.io/badge/Vite-7.x-646cff?style=flat-square&logo=vite)](https://vitejs.dev/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![Deploy with Vercel](https://img.shields.io/badge/Deploy-Vercel-black?style=flat-square&logo=vercel)](https://corporatelawfirm.vercel.app)

## 🌐 Live Demo

### **🚀 [https://corporatelawfirm.vercel.app](https://corporatelawfirm.vercel.app)**

> Deployed on Vercel with automatic CI/CD from GitHub

## 🎯 Overview

This project showcases a complete law firm website with a focus on modern web design principles, user experience, and performance optimization. Built using Vue 3's Composition API and powered by Vite for lightning-fast development and build times.

## ✨ Features

- **🎨 Modern Design**: Clean, professional interface with elegant typography and sophisticated color scheme
- **📱 Fully Responsive**: Seamless experience across all devices (mobile, tablet, desktop)
- **⚡ Performance Optimized**: Built with Vite for exceptional loading speeds and runtime performance
- **🎭 Rich Animations**: Smooth scroll effects, fade-in transitions, and engaging hover interactions
- **🧩 Component-Based Architecture**: Modular Vue 3 components using Composition API
- **♿ Accessibility Focused**: Semantic HTML5, ARIA labels, and keyboard navigation support
- **🔍 SEO Ready**: Optimized meta tags and semantic structure for search engines
- **🎨 Glassmorphism UI**: Modern glass-effect designs in key sections

## 🏗️ Project Structure

```
corporatelawfirm/
├── public/
│   └── vite.svg
├── src/
│   ├── components/
│   │   ├── Header.vue          # Sticky navigation with mobile menu
│   │   ├── Hero.vue            # Hero section with CTA
│   │   ├── Expertise.vue       # Services grid showcase
│   │   ├── Team.vue            # Attorney profiles
│   │   ├── Contact.vue         # Contact form and info
│   │   └── Footer.vue          # Site footer
│   ├── App.vue                 # Root component
│   ├── main.js                 # Application entry point
│   └── style.css               # Global styles and variables
├── index.html                  # HTML template
├── package.json                # Dependencies and scripts
├── vite.config.js             # Vite configuration
└── README.md                   # Project documentation
```

## 🚀 Quick Start

### Prerequisites

- Node.js 16.x or higher
- npm or yarn package manager

### Installation

```bash
# Clone the repository
git clone https://github.com/onurceyhan/corporatelawfirm.git

# Navigate to project directory
cd corporatelawfirm

# Install dependencies
npm install

# Start development server
npm run dev
```

The application will be available at `http://localhost:5173/`

### Build for Production

```bash
# Create optimized production build
npm run build

# Preview production build locally
npm run preview
```

### Deploy to Vercel

This project is configured for easy deployment on Vercel:

```bash
# Install Vercel CLI globally
npm install -g vercel

# Deploy to Vercel
vercel

# Deploy to production
vercel --prod
```

Alternatively, you can connect your GitHub repository to Vercel for automatic deployments on every push to the main branch.

## 📦 Component Overview

### Header
- Fixed navigation bar with scroll effects
- Transparent overlay transitioning to solid background on scroll
- Responsive mobile menu with slide-in animation
- Smooth scroll navigation to page sections

### Hero Section
- Full-viewport hero with high-quality imagery
- Animated typography with staggered entrance effects
- Prominent call-to-action button
- Decorative animated elements
- Scroll indicator

### Expertise (Services)
- Grid layout showcasing six practice areas
- Interactive service cards with hover effects
- Icon-based visual hierarchy
- Detailed service descriptions

### Team
- Attorney profile cards with professional photography
- Image hover overlays with social media links
- Responsive grid layout adapting to screen size
- Professional credentials and specializations

### Contact
- Two-column layout with contact information and form
- Modern form design with glassmorphism effect
- Service selection dropdown
- Contact details with office hours
- Form validation

### Footer
- Four-column layout with organized information
- Practice areas quick links
- Social media integration
- Contact information
- Copyright and legal links

## 🛠️ Technology Stack

| Technology | Purpose |
|------------|---------|
| **Vue 3** | Progressive JavaScript framework with Composition API |
| **Vite** | Next-generation frontend build tool |
| **JavaScript (ES6+)** | Modern JavaScript features |
| **CSS3** | Advanced styling with animations and transitions |
| **Google Fonts** | Playfair Display (headings) & Inter (body text) |
| **Unsplash API** | High-quality stock photography |

## 🎨 Design System

### Color Palette

```css
Primary Gold:       #c9a961  /* Accent color for CTAs and highlights */
Dark Gold:          #b8954d  /* Hover states and secondary accents */
Dark Background:    #1a1a1a  /* Primary dark backgrounds */
Secondary Dark:     #2c3e50  /* Section backgrounds */
Text Dark:          #1a1a1a  /* Primary text color */
Text Gray:          #666     /* Secondary text color */
Light Background:   #f8f9fa  /* Light section backgrounds */
```

### Typography

- **Headings**: Playfair Display (serif) - Elegant and authoritative
- **Body Text**: Inter (sans-serif) - Clean and highly readable
- **Font Weights**: 300 (light), 400 (regular), 500 (medium), 600 (semi-bold), 700 (bold)

### Responsive Breakpoints

```css
Mobile:     < 768px   /* Single column layouts */
Tablet:     768px - 968px  /* Two-column layouts */
Desktop:    > 968px   /* Full multi-column layouts */
```

## ⚙️ Configuration

### Customizing Colors

Edit the CSS variables in `src/style.css`:

```css
:root {
  --primary-gold: #c9a961;
  --dark-gold: #b8954d;
  --dark-bg: #1a1a1a;
  --dark-secondary: #2c3e50;
  --text-dark: #1a1a1a;
  --text-gray: #666;
  --light-bg: #f8f9fa;
}
```

### Modifying Content

Each component is self-contained in `src/components/`. Update the content directly in the component files:

- Service offerings in `Expertise.vue`
- Team member information in `Team.vue`
- Contact details in `Contact.vue` and `Footer.vue`

### Changing Images

Replace Unsplash URLs in:
- `Hero.vue` - Background image
- `Team.vue` - Attorney profile photos

## 🌐 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## 📈 Performance

- **Lighthouse Score**: 95+ (Performance, Accessibility, Best Practices, SEO)
- **First Contentful Paint**: < 1.2s
- **Time to Interactive**: < 2.5s
- **Bundle Size**: Optimized with code splitting and tree shaking

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Onur Ceyhan**
- 🔗 GitHub: [@onurceyhan](https://github.com/onurceyhan)
- 💼 LinkedIn: [onur-ceyhan](https://www.linkedin.com/in/onur-ceyhan/)
- 📁 Project Repository: [corporatelawfirm](https://github.com/onurceyhan/corporatelawfirm)

## 🙏 Acknowledgments

- Design inspiration from modern law firm websites
- Photography from [Unsplash](https://unsplash.com)
- Icons and fonts from Google Fonts
- Vue.js and Vite communities

---

<p align="center">Made with ❤️ using Vue 3 & Vite</p>
<p align="center">
  <a href="https://corporatelawfirm.vercel.app">Live Demo</a> • 
  <a href="https://github.com/onurceyhan/corporatelawfirm">GitHub</a> • 
  <a href="https://www.linkedin.com/in/onur-ceyhan/">LinkedIn</a>
</p>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'
import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import MenuSection from './components/MenuSection.vue'
import ReserveSection from './components/ReserveSection.vue'
import ContactSection from './components/ContactSection.vue'
import FooterSection from './components/FooterSection.vue'

const scrolled = ref(false)
let ticking = false

function onScroll() {
  if (!ticking) {
    requestAnimationFrame(() => {
      scrolled.value = window.scrollY > 60
      ticking = false
    })
    ticking = true
  }
}

function scrollTo(id: string) {
  const el = document.querySelector(id)
  if (el) {
    el.scrollIntoView({ behavior: 'smooth' })
  }
}

onMounted(() => window.addEventListener('scroll', onScroll))
onUnmounted(() => window.removeEventListener('scroll', onScroll))
</script>

<template>
  <NavBar :scrolled="scrolled" @navigate="scrollTo" />
  <HeroSection @navigate="scrollTo" />
  <AboutSection />
  <MenuSection />
  <ReserveSection />
  <ContactSection />
  <FooterSection />
</template>

<style>
/* ── Reset & Global ── */
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
html {
  scroll-behavior: smooth;
}
body {
  font-family: 'Inter', 'Noto Serif SC', system-ui, -apple-system, sans-serif;
  color: #1a1a1a;
  background: #faf9f7;
  -webkit-font-smoothing: antialiased;
}
img {
  display: block;
  max-width: 100%;
}
a {
  text-decoration: none;
  color: inherit;
}
ul {
  list-style: none;
}
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 24px;
}
section {
  padding: 100px 0;
}
.section-header {
  text-align: center;
  margin-bottom: 64px;
}
.section-tag {
  font-size: 12px;
  letter-spacing: 4px;
  text-transform: uppercase;
  color: #c8a87c;
  font-weight: 500;
  margin-bottom: 12px;
}
.section-title {
  font-family: 'Noto Serif SC', serif;
  font-size: clamp(28px, 4vw, 38px);
  font-weight: 600;
  letter-spacing: 4px;
  color: #1a1a1a;
}
.section-desc {
  max-width: 520px;
  margin: 16px auto 0;
  font-size: 15px;
  color: #666;
  line-height: 1.7;
  font-weight: 300;
}
@keyframes scrollIn {
  0%,
  100% {
    transform: scaleY(0.5);
    opacity: 0.4;
  }
  50% {
    transform: scaleY(1);
    opacity: 1;
  }
}
@media (max-width: 820px) {
  .nav-links { display: none }
  .about-grid { grid-template-columns: 1fr; gap: 40px }
  .about-image { height: 320px }
  .dishes { grid-template-columns: 1fr; max-width: 480px; margin: 0 auto }
  .reserve-card { padding: 32px 20px }
  .contact-grid { grid-template-columns: 1fr }
  .reserve-card .info-row { flex-direction: column; gap: 4px; align-items: flex-start }
}
@media (max-width: 480px) {
  section { padding: 64px 0 }
  .hero-title { letter-spacing: 6px }
  .about-image { height: 240px }
  .dish-img { height: 200px }
}
</style>

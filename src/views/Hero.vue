<script setup>
import ccsLogo from '../assets/LOGO.png'
</script>

<template>
  <section id="hero" class="hero">
    <div class="hero-backdrop" aria-hidden="true">
      <img :src="ccsLogo" alt="" />
    </div>

    <div class="hero-content">
      <p class="tagline">the CCS core practices that build bridges between gaps</p>
      <h1>REMEMBER<br />CONNECT<br />ENGAGE<br />BUILD<br />SHARE</h1>
      <p class="motto">different PEOPLE, ONE goal</p>
      <a class="hero-button" href="#programs">Your FUTURE begins HERE</a>
    </div>
  </section>
</template>

<style scoped>
.hero {
  min-height: 470px;
  position: relative;
  display: flex;
  align-items: center;
  overflow: hidden;
  isolation: isolate;
  padding: 5rem max(2rem, calc((100vw - 650px) / 2));
  color: #f8fafc;
  background: #363636;
}

.hero-backdrop {
  position: absolute;
  z-index: -1;
  inset: 0;
  display: grid;
  place-items: center;
  overflow: hidden;
  background:
    radial-gradient(ellipse at 62% 48%, rgba, transparent 48%),
    #363636;
}

.hero-backdrop img {
  width: min(64vw, 790px);
  height: min(64vw, 790px);
  object-fit: cover;
  opacity: 0.075;
  filter: grayscale(1) brightness(2.2);
  transform: rotate(-12deg) scale(1.2);
}

.hero-content {
  width: 100%;
  max-width: 650px;
  margin: 0 auto;
  padding-left: 1.25rem;
}

.tagline {
  margin: 0 0 0.8rem;
  color: #cbd5d1;
  font-size: 0.8rem;
}

h1 {
  margin: 0;
  font-size: clamp(2rem, 4vw, 3.1rem);
  font-weight: 800;
  line-height: 0.98;
  letter-spacing: -0.035em;
}

.motto {
  margin: 0.8rem 0 2rem;
  color: #e3e3e3;
  font-size: 1.1rem;
}

.hero-button {
  display: inline-block;
  padding: 0.75rem 1.2rem;
  border-radius: 3px;
  background: #e3e3e3;
  color: #132526;
  font-size: 0.85rem;
  font-weight: 700;
  text-decoration: none;
  transition: background-color 0.2s ease, transform 0.2s ease;
}

.hero-button:hover {
  background: #ffc247;
  transform: translateY(-2px);
}

@media (max-width: 640px) {
  .hero {
    min-height: 440px;
    padding: 5rem 1.5rem 3rem;
  }

  .hero-content {
    padding-left: 0;
  }

  .hero-backdrop img {
    width: 110vw;
    height: 110vw;
  }
}
</style>

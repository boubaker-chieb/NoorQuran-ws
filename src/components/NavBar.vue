<template>
  <nav class="navbar" :class="{ scrolled }">
    <div class="container nav-inner">
      <router-link to="/" class="nav-brand">
        <div class="brand-icon">
          <img src="/logo.svg" alt="NoorQuran Logo" width="36" height="36" />
        </div>
        <span class="brand-text">NoorQuran</span>
      </router-link>

      <div class="nav-links hide-mobile">
        <a href="#features">Features</a>
        <a href="#screenshots">Screenshots</a>
        <a href="#download">Download</a>
        <router-link to="/privacy">Privacy</router-link>
      </div>

      <a href="#download" class="btn btn-primary nav-cta hide-mobile">
        <svg
          width="18"
          height="18"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2.5"
          stroke-linecap="round"
          stroke-linejoin="round"
        >
          <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4" />
          <polyline points="7 10 12 15 17 10" />
          <line x1="12" y1="15" x2="12" y2="3" />
        </svg>
        Download
      </a>

      <!-- Mobile hamburger -->
      <button
        class="nav-toggle hide-desktop"
        @click="menuOpen = !menuOpen"
        :aria-label="menuOpen ? 'Close menu' : 'Open menu'"
      >
        <span :class="{ open: menuOpen }"></span>
      </button>
    </div>

    <!-- Mobile menu -->
    <transition name="slide-down">
      <div v-if="menuOpen" class="mobile-menu hide-desktop">
        <a href="#features" @click="menuOpen = false">Features</a>
        <a href="#screenshots" @click="menuOpen = false">Screenshots</a>
        <a href="#download" @click="menuOpen = false">Download</a>
        <router-link to="/privacy" @click="menuOpen = false"
          >Privacy Policy</router-link
        >
      </div>
    </transition>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const scrolled = ref(false);
const menuOpen = ref(false);

function handleScroll() {
  scrolled.value = window.scrollY > 20;
}

onMounted(() => window.addEventListener("scroll", handleScroll));
onUnmounted(() => window.removeEventListener("scroll", handleScroll));
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  padding: 1rem 0;
  transition: all 0.35s var(--ease);
  background: transparent;
}

.navbar.scrolled {
  background: rgba(249, 246, 241, 0.92);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  padding: 0.6rem 0;
  box-shadow: 0 1px 16px var(--shadow);
}

.nav-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav-brand {
  display: flex;
  align-items: center;
  gap: 0.65rem;
  text-decoration: none;
}

.brand-icon {
  display: flex;
  align-items: center;
  transition: transform var(--duration) var(--ease);
}

.nav-brand:hover .brand-icon {
  transform: rotate(8deg) scale(1.05);
}

.brand-text {
  font-size: 1.3rem;
  font-weight: 800;
  color: var(--text);
  letter-spacing: -0.02em;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 2.25rem;
}

.nav-links a {
  font-size: 0.92rem;
  font-weight: 500;
  color: var(--text-secondary);
  transition: color var(--duration) var(--ease);
  text-decoration: none;
}

.nav-links a:hover {
  color: var(--primary);
}

.nav-cta {
  padding: 0.65rem 1.5rem;
  font-size: 0.9rem;
}

/* Hamburger */
.nav-toggle {
  width: 36px;
  height: 36px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0;
}

.nav-toggle span,
.nav-toggle span::before,
.nav-toggle span::after {
  display: block;
  width: 22px;
  height: 2px;
  background: var(--text);
  border-radius: 2px;
  transition: all 0.3s var(--ease);
  position: relative;
}

.nav-toggle span::before,
.nav-toggle span::after {
  content: "";
  position: absolute;
  left: 0;
}

.nav-toggle span::before {
  top: -7px;
}
.nav-toggle span::after {
  top: 7px;
}

.nav-toggle span.open {
  background: transparent;
}
.nav-toggle span.open::before {
  top: 0;
  transform: rotate(45deg);
  background: var(--primary);
}
.nav-toggle span.open::after {
  top: 0;
  transform: rotate(-45deg);
  background: var(--primary);
}

/* Mobile menu */
.mobile-menu {
  background: var(--surface);
  border-top: 1px solid var(--border-light);
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
}

.mobile-menu a {
  font-size: 1.05rem;
  font-weight: 500;
  color: var(--text);
  text-decoration: none;
  padding: 0.5rem 0;
  border-bottom: 1px solid var(--border-light);
}

.slide-down-enter-active,
.slide-down-leave-active {
  transition: all 0.3s var(--ease);
}
.slide-down-enter-from,
.slide-down-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>

<template>
  <main>
    <!-- ═══════ HERO SECTION ═══════ -->
    <section class="hero pattern-bg">
      <!-- Floating decorative elements -->
      <div class="hero-decor">
        <div class="decor-star star-1">✦</div>
        <div class="decor-star star-2">✧</div>
        <div class="decor-star star-3">✦</div>
        <div class="decor-crescent">☪</div>
        <div class="decor-circle circle-1"></div>
        <div class="decor-circle circle-2"></div>
      </div>

      <div class="container hero-inner">
        <div class="hero-content">
          <div class="hero-badge">
            <span class="badge-dot"></span>
            Available on Android & iOS
          </div>

          <h1 class="hero-title">
            Your Complete<br />
            <span class="gradient-text">Quran Companion</span>
          </h1>

          <p class="hero-arabic arabic-text">﴿ إِنَّا نَحْنُ نَزَّلْنَا ٱلذِّكْرَ وَإِنَّا لَهُۥ لَحَـٰفِظُونَ ﴾</p>
          <p class="hero-verse-ref">— Surah Al-Hijr (15:9)</p>

          <p class="subtitle hero-desc">
            Read the Holy Quran with beautiful Tajweed, listen to world-renowned reciters,
            track your prayer times, and deepen your connection with Allah — all in one beautifully designed app.
          </p>

          <div class="hero-actions">
            <a href="https://play.google.com/store/apps/details?id=com.boubakerchieb.noorquran" target="_blank" rel="noopener" class="store-btn google-play">
              <svg viewBox="0 0 24 24" width="24" height="24" fill="currentColor">
                <path d="M3.609 1.814L13.792 12 3.61 22.186a.996.996 0 0 1-.61-.92V2.734a1 1 0 0 1 .609-.92zm10.89 10.893l2.302 2.302-10.937 6.333 8.635-8.635zm3.199-3.199l2.302 2.302-2.302 2.302-2.794-2.302 2.794-2.302zM5.864 2.658L16.8 8.99l-2.302 2.302L5.864 2.658z"/>
              </svg>
              <div>
                <small>GET IT ON</small>
                <strong>Google Play</strong>
              </div>
            </a>
            <a href="#" class="store-btn app-store">
              <svg viewBox="0 0 24 24" width="24" height="24" fill="currentColor">
                <path d="M18.71 19.5c-.83 1.24-1.71 2.45-3.05 2.47-1.34.03-1.77-.79-3.29-.79-1.53 0-2 .77-3.27.82-1.31.05-2.3-1.32-3.14-2.53C4.25 17 2.94 12.45 4.7 9.39c.87-1.52 2.43-2.48 4.12-2.51 1.28-.02 2.5.87 3.29.87.78 0 2.26-1.07 3.8-.91.65.03 2.47.26 3.64 1.98-.09.06-2.17 1.28-2.15 3.81.03 3.02 2.65 4.03 2.68 4.04-.03.07-.42 1.44-1.38 2.83M13 3.5c.73-.83 1.94-1.46 2.94-1.5.13 1.17-.34 2.35-1.04 3.19-.69.85-1.83 1.51-2.95 1.42-.15-1.15.41-2.35 1.05-3.11z"/>
              </svg>
              <div>
                <small>COMING SOON ON</small>
                <strong>App Store</strong>
              </div>
            </a>
          </div>

          <div class="hero-stats">
            <div class="stat">
              <strong>114</strong>
              <span>Surahs</span>
            </div>
            <div class="stat-divider"></div>
            <div class="stat">
              <strong>8</strong>
              <span>Languages</span>
            </div>
            <div class="stat-divider"></div>
            <div class="stat">
              <strong>7+</strong>
              <span>Reciters</span>
            </div>
          </div>
        </div>

        <div class="hero-visual">
          <div class="phone-mockup">
            <div class="phone-frame">
              <div class="phone-screen">
                <img src="/screenshots/1.png" alt="NoorQuran App" class="phone-screenshot" />
              </div>
            </div>
            <!-- Glow effect -->
            <div class="phone-glow"></div>
          </div>
        </div>
      </div>
    </section>

    <!-- ═══════ FEATURES SECTION ═══════ -->
    <section id="features" class="section section-alt">
      <div class="container">
        <div class="text-center reveal">
          <span class="section-label">Features</span>
          <h2>Everything You Need for<br /><span class="gradient-text">Your Spiritual Journey</span></h2>
          <p class="subtitle" style="margin: 1rem auto 0;">Crafted with love and attention to detail for the best Quran reading experience.</p>
        </div>

        <div class="features-grid">
          <div v-for="(feature, i) in features" :key="i" class="feature-card card reveal" :style="{ transitionDelay: `${i * 0.1}s` }">
            <div class="feature-icon" :style="{ background: feature.bg }">
              <span v-html="feature.icon"></span>
            </div>
            <h3>{{ feature.title }}</h3>
            <p>{{ feature.desc }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- ═══════ SHOWCASE / SCREENSHOTS SECTION ═══════ -->
    <section id="screenshots" class="section pattern-bg">
      <div class="container">
        <div class="text-center reveal">
          <span class="section-label">Showcase</span>
          <h2>Beautiful & Intuitive<br /><span class="gradient-text">Islamic Design</span></h2>
          <p class="subtitle" style="margin: 1rem auto 0;">Every detail crafted with Islamic aesthetics in mind — from the geometric patterns to the golden ornaments.</p>
        </div>

        <div class="showcase-row reveal">
          <div class="showcase-card" v-for="(item, i) in showcaseItems" :key="i">
            <div class="showcase-phone">
              <div class="showcase-screen">
                <img :src="item.image" :alt="item.label" class="showcase-img" />
              </div>
            </div>
            <p class="showcase-label">{{ item.label }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- ═══════ LANGUAGES SECTION ═══════ -->
    <section class="section section-alt">
      <div class="container">
        <div class="languages-layout reveal">
          <div class="languages-info">
            <span class="section-label">Global</span>
            <h2>Available in<br /><span class="gradient-text">8 Languages</span></h2>
            <p class="subtitle">NoorQuran speaks your language. The entire app interface is translated, making the Quran accessible to Muslims worldwide.</p>
          </div>
          <div class="languages-grid">
            <div v-for="(lang, i) in languages" :key="i" class="lang-chip" :style="{ animationDelay: `${i * 0.1}s` }">
              <span class="lang-flag">{{ lang.flag }}</span>
              <div>
                <strong>{{ lang.name }}</strong>
                <small>{{ lang.native }}</small>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ═══════ PREMIUM SECTION ═══════ -->
    <section class="section premium-section pattern-bg">
      <div class="container">
        <div class="premium-card reveal">
          <div class="premium-glow"></div>
          <div class="premium-content">
            <div class="premium-badge">
              <span>💎</span> Premium
            </div>
            <h2>Unlock the Full<br /><span class="gold-text">NoorQuran Experience</span></h2>
            <p class="subtitle" style="color: rgba(255,255,255,0.8);">Get access to all reciters, every adhan sound, and background audio playback.</p>

            <div class="premium-features">
              <div class="pf-item">
                <span class="pf-icon">🎙️</span>
                <div>
                  <strong>All Reciters</strong>
                  <p>Listen to every world-renowned reciter</p>
                </div>
              </div>
              <div class="pf-item">
                <span class="pf-icon">🕌</span>
                <div>
                  <strong>All Adhan Sounds</strong>
                  <p>Makkah, Madinah, Al-Aqsa & more</p>
                </div>
              </div>
              <div class="pf-item">
                <span class="pf-icon">🎵</span>
                <div>
                  <strong>Background Audio</strong>
                  <p>Keep listening while using other apps</p>
                </div>
              </div>
            </div>

            <div class="premium-plans">
              <div class="plan-chip">
                <span>Monthly</span>
                <strong>$1.99</strong>
              </div>
              <div class="plan-chip popular">
                <div class="plan-badge">Best Value</div>
                <span>Yearly</span>
                <strong>$7.99</strong>
              </div>
              <div class="plan-chip">
                <span>Lifetime</span>
                <strong>$19.99</strong>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ═══════ DOWNLOAD CTA SECTION ═══════ -->
    <section id="download" class="section">
      <div class="container">
        <div class="cta-card reveal">
          <div class="cta-decor">
            <span class="cta-star">✦</span>
            <span class="cta-star">✧</span>
            <span class="cta-star">✦</span>
          </div>
          <h2>Start Your Journey<br />with <span class="gradient-text">NoorQuran</span></h2>
          <p class="subtitle" style="margin: 0.5rem auto 2rem; text-align: center;">Download free today and bring the Quran closer to your heart.</p>

          <div class="cta-buttons">
            <a href="https://play.google.com/store/apps/details?id=com.boubakerchieb.noorquran" target="_blank" rel="noopener" class="btn btn-primary btn-lg">
              <svg viewBox="0 0 24 24" width="22" height="22" fill="currentColor"><path d="M3.609 1.814L13.792 12 3.61 22.186a.996.996 0 0 1-.61-.92V2.734a1 1 0 0 1 .609-.92zm10.89 10.893l2.302 2.302-10.937 6.333 8.635-8.635zm3.199-3.199l2.302 2.302-2.302 2.302-2.794-2.302 2.794-2.302zM5.864 2.658L16.8 8.99l-2.302 2.302L5.864 2.658z"/></svg>
              Google Play
            </a>
            <a href="#" class="btn btn-outline btn-lg">
              <svg viewBox="0 0 24 24" width="22" height="22" fill="currentColor"><path d="M18.71 19.5c-.83 1.24-1.71 2.45-3.05 2.47-1.34.03-1.77-.79-3.29-.79-1.53 0-2 .77-3.27.82-1.31.05-2.3-1.32-3.14-2.53C4.25 17 2.94 12.45 4.7 9.39c.87-1.52 2.43-2.48 4.12-2.51 1.28-.02 2.5.87 3.29.87.78 0 2.26-1.07 3.8-.91.65.03 2.47.26 3.64 1.98-.09.06-2.17 1.28-2.15 3.81.03 3.02 2.65 4.03 2.68 4.04-.03.07-.42 1.44-1.38 2.83M13 3.5c.73-.83 1.94-1.46 2.94-1.5.13 1.17-.34 2.35-1.04 3.19-.69.85-1.83 1.51-2.95 1.42-.15-1.15.41-2.35 1.05-3.11z"/></svg>
              App Store (Soon)
            </a>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script setup>
import { onMounted } from 'vue'

const features = [
  {
    icon: '📖',
    title: 'Full Quran with Tajweed',
    desc: 'Read all 114 Surahs with color-coded Tajweed rules for perfect pronunciation.',
    bg: 'linear-gradient(135deg, #E8F5F1, #D4EDE7)',
  },
  {
    icon: '🎧',
    title: 'Audio Recitation',
    desc: 'Listen to beautiful recitations from world-renowned Qaris with verse-by-verse playback.',
    bg: 'linear-gradient(135deg, #FEF3E2, #FDE8C8)',
  },
  {
    icon: '🕌',
    title: 'Prayer Times',
    desc: 'Accurate prayer times based on your location with customizable notification alerts.',
    bg: 'linear-gradient(135deg, #E8EAF6, #C5CAE9)',
  },
  {
    icon: '🧭',
    title: 'Qibla Compass',
    desc: 'Find the exact direction of the Kaaba from anywhere in the world with precision.',
    bg: 'linear-gradient(135deg, #FFF3E0, #FFE0B2)',
  },
  {
    icon: '🔖',
    title: 'Bookmarks',
    desc: 'Save and organize your favorite verses for quick access during study or reflection.',
    bg: 'linear-gradient(135deg, #FCE4EC, #F8BBD0)',
  },
  {
    icon: '🌙',
    title: 'Ramadan Theme',
    desc: 'Special emerald & gold Ramadan theme with animated stars, lanterns, and crescent effects.',
    bg: 'linear-gradient(135deg, #E8F5E9, #C8E6C9)',
  },
  {
    icon: '📅',
    title: 'Hijri Calendar',
    desc: 'Display the current Hijri date alongside Gregorian — never miss an Islamic occasion.',
    bg: 'linear-gradient(135deg, #F3E5F5, #E1BEE7)',
  },
  {
    icon: '🌍',
    title: '8 Languages',
    desc: 'Full app interface in English, Arabic, French, Spanish, Turkish, Urdu, Indonesian & Bengali.',
    bg: 'linear-gradient(135deg, #E0F7FA, #B2EBF2)',
  },
]

const showcaseItems = [
  { image: '/screenshots/1.png', label: 'Quran Reader' },
  { image: '/screenshots/2.png', label: 'Prayer Times' },
  { image: '/screenshots/3.png', label: 'Qibla' },
  { image: '/screenshots/4.png', label: 'Bookmarks' },
  { image: '/screenshots/5.png', label: 'Settings' },
  { image: '/screenshots/6.png', label: 'Recitation' },
  { image: '/screenshots/7.png', label: 'More' },
]

const languages = [
  { flag: '🇬🇧', name: 'English', native: 'English' },
  { flag: '🇸🇦', name: 'Arabic', native: 'العربية' },
  { flag: '🇫🇷', name: 'French', native: 'Français' },
  { flag: '🇪🇸', name: 'Spanish', native: 'Español' },
  { flag: '🇹🇷', name: 'Turkish', native: 'Türkçe' },
  { flag: '🇵🇰', name: 'Urdu', native: 'اردو' },
  { flag: '🇮🇩', name: 'Indonesian', native: 'Bahasa' },
  { flag: '🇧🇩', name: 'Bengali', native: 'বাংলা' },
]

// Intersection Observer for scroll reveal
onMounted(() => {
  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible')
        }
      })
    },
    { threshold: 0.1, rootMargin: '0px 0px -40px 0px' }
  )

  document.querySelectorAll('.reveal').forEach((el) => observer.observe(el))
})
</script>

<style scoped>
/* ═══════════════════════════════════════════════
   HERO
   ═══════════════════════════════════════════════ */
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  padding: 8rem 0 4rem;
  overflow: hidden;
}

.hero-inner {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
}

.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: var(--primary-50);
  color: var(--primary);
  font-size: 0.85rem;
  font-weight: 600;
  padding: 0.5rem 1.2rem;
  border-radius: 100px;
  border: 1px solid var(--primary-10);
  margin-bottom: 1.5rem;
}

.badge-dot {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: var(--success);
  animation: pulse-glow 2s infinite;
}

.hero-title {
  margin-bottom: 1.5rem;
  line-height: 1.1;
}

.gradient-text {
  background: linear-gradient(135deg, var(--primary), var(--gold));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.gold-text {
  background: linear-gradient(135deg, var(--gold), var(--accent));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero-arabic {
  font-size: clamp(1.1rem, 2vw, 1.4rem);
  color: var(--gold-dark);
  margin-bottom: 0.25rem;
  opacity: 0.8;
}

.hero-verse-ref {
  font-size: 0.85rem;
  color: var(--text-tertiary);
  margin-bottom: 1.5rem;
}

.hero-desc {
  margin-bottom: 2rem;
}

/* Store buttons */
.hero-actions {
  display: flex;
  gap: 1rem;
  margin-bottom: 2.5rem;
  flex-wrap: wrap;
}

.store-btn {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  padding: 0.75rem 1.5rem;
  border-radius: var(--radius);
  text-decoration: none;
  transition: all var(--duration) var(--ease);
  border: 2px solid transparent;
}

.store-btn small {
  display: block;
  font-size: 0.65rem;
  font-weight: 600;
  letter-spacing: 0.05em;
  text-transform: uppercase;
  opacity: 0.8;
}

.store-btn strong {
  display: block;
  font-size: 1.05rem;
  font-weight: 700;
  line-height: 1.2;
}

.google-play {
  background: var(--text);
  color: #fff;
}

.google-play:hover {
  background: #000;
  color: #fff;
  transform: translateY(-2px);
  box-shadow: 0 8px 24px var(--shadow-lg);
}

.app-store {
  background: transparent;
  color: var(--text);
  border-color: var(--border);
}

.app-store:hover {
  border-color: var(--primary);
  color: var(--primary);
  transform: translateY(-2px);
}

/* Stats */
.hero-stats {
  display: flex;
  align-items: center;
  gap: 1.5rem;
}

.stat {
  text-align: center;
}

.stat strong {
  display: block;
  font-size: 1.6rem;
  font-weight: 800;
  color: var(--primary);
}

.stat span {
  font-size: 0.82rem;
  color: var(--text-tertiary);
  font-weight: 500;
}

.stat-divider {
  width: 1px;
  height: 32px;
  background: var(--border);
}

/* Phone mockup */
.hero-visual {
  display: flex;
  justify-content: center;
  position: relative;
}

.phone-mockup {
  position: relative;
  animation: float 6s ease-in-out infinite;
}

.phone-frame {
  width: 280px;
  height: 560px;
  background: #1a1a1a;
  border-radius: 40px;
  padding: 12px;
  box-shadow:
    0 0 0 2px #333,
    0 30px 60px rgba(0, 0, 0, 0.2),
    0 0 0 12px rgba(13, 124, 102, 0.05);
  position: relative;
  z-index: 2;
}

.phone-screen {
  width: 100%;
  height: 100%;
  border-radius: 30px;
  overflow: hidden;
  background: #000;
}

.phone-screenshot {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.phone-glow {
  position: absolute;
  inset: -20%;
  background: radial-gradient(circle, var(--primary-20) 0%, transparent 70%);
  z-index: 1;
  filter: blur(40px);
  animation: pulse-glow 4s ease-in-out infinite;
}

/* Floating decor */
.hero-decor {
  position: absolute;
  inset: 0;
  pointer-events: none;
  z-index: 0;
}

.decor-star {
  position: absolute;
  color: var(--gold);
  font-size: 1.2rem;
  animation: star-twinkle 3s ease-in-out infinite;
}

.star-1 { top: 15%; left: 8%; animation-delay: 0s; }
.star-2 { top: 25%; right: 10%; animation-delay: 1s; font-size: 0.9rem; }
.star-3 { bottom: 20%; left: 15%; animation-delay: 2s; }

.decor-crescent {
  position: absolute;
  top: 10%;
  right: 15%;
  font-size: 2rem;
  color: var(--gold);
  opacity: 0.15;
  animation: float 8s ease-in-out infinite;
}

.decor-circle {
  position: absolute;
  border-radius: 50%;
  border: 1px solid var(--primary-10);
}

.circle-1 {
  width: 300px;
  height: 300px;
  bottom: -100px;
  left: -100px;
  animation: rotate-slow 30s linear infinite;
}

.circle-2 {
  width: 200px;
  height: 200px;
  top: 10%;
  right: -50px;
  border-color: var(--gold-50);
  opacity: 0.3;
  animation: rotate-slow 25s linear infinite reverse;
}

/* ═══════════════════════════════════════════════
   FEATURES
   ═══════════════════════════════════════════════ */
.features-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1.5rem;
  margin-top: 4rem;
}

.feature-card {
  text-align: center;
  padding: 2.5rem 1.5rem;
}

.feature-icon {
  width: 72px;
  height: 72px;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2rem;
  margin: 0 auto 1.25rem;
}

.feature-card h3 {
  font-size: 1.1rem;
  font-weight: 700;
  margin-bottom: 0.6rem;
}

.feature-card p {
  font-size: 0.9rem;
  color: var(--text-secondary);
  line-height: 1.6;
}

/* ═══════════════════════════════════════════════
   SHOWCASE
   ═══════════════════════════════════════════════ */
.showcase-row {
  display: flex;
  gap: 2rem;
  margin-top: 4rem;
  justify-content: center;
  flex-wrap: wrap;
}

.showcase-card {
  text-align: center;
}

.showcase-phone {
  width: 160px;
  height: 300px;
  background: #1a1a1a;
  border-radius: 24px;
  padding: 8px;
  box-shadow: 0 16px 40px var(--shadow-lg);
  transition: all var(--duration) var(--ease);
}

.showcase-card:hover .showcase-phone {
  transform: translateY(-8px) scale(1.02);
  box-shadow: 0 24px 60px var(--shadow-lg);
}

.showcase-screen {
  width: 100%;
  height: 100%;
  border-radius: 18px;
  overflow: hidden;
}

.showcase-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.showcase-label {
  margin-top: 0.75rem;
  font-size: 0.85rem;
  font-weight: 600;
  color: var(--text-secondary);
}

/* ═══════════════════════════════════════════════
   LANGUAGES
   ═══════════════════════════════════════════════ */
.languages-layout {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
}

.languages-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}

.lang-chip {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  padding: 1rem 1.25rem;
  background: var(--surface);
  border: 1px solid var(--border-light);
  border-radius: var(--radius);
  transition: all var(--duration) var(--ease);
}

.lang-chip:hover {
  border-color: var(--primary-20);
  transform: translateY(-2px);
  box-shadow: 0 8px 24px var(--shadow);
}

.lang-flag {
  font-size: 1.75rem;
}

.lang-chip strong {
  display: block;
  font-size: 0.95rem;
  color: var(--text);
}

.lang-chip small {
  font-size: 0.8rem;
  color: var(--text-tertiary);
}

/* ═══════════════════════════════════════════════
   PREMIUM
   ═══════════════════════════════════════════════ */
.premium-section {
  padding: 0;
}

.premium-card {
  background: linear-gradient(135deg, #0D7C66, #095C4B 40%, #06382D);
  border-radius: var(--radius-xl);
  padding: clamp(3rem, 6vw, 5rem);
  position: relative;
  overflow: hidden;
  color: white;
}

.premium-glow {
  position: absolute;
  top: -50%;
  right: -20%;
  width: 400px;
  height: 400px;
  background: radial-gradient(circle, rgba(200, 169, 126, 0.2), transparent 70%);
  filter: blur(60px);
  pointer-events: none;
}

.premium-content {
  position: relative;
  z-index: 2;
  max-width: 700px;
}

.premium-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(10px);
  padding: 0.5rem 1.25rem;
  border-radius: 100px;
  font-size: 0.85rem;
  font-weight: 700;
  color: var(--gold);
  margin-bottom: 1.5rem;
  border: 1px solid rgba(200, 169, 126, 0.3);
}

.premium-card h2 {
  color: white;
  margin-bottom: 1rem;
}

.premium-features {
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
  margin: 2.5rem 0;
}

.pf-item {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
}

.pf-icon {
  font-size: 1.5rem;
  flex-shrink: 0;
  margin-top: 0.1rem;
}

.pf-item strong {
  display: block;
  font-size: 1rem;
  margin-bottom: 0.15rem;
}

.pf-item p {
  font-size: 0.88rem;
  color: rgba(255, 255, 255, 0.65);
  margin: 0;
}

.premium-plans {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

.plan-chip {
  background: rgba(255, 255, 255, 0.1);
  border: 1px solid rgba(255, 255, 255, 0.15);
  border-radius: var(--radius);
  padding: 1rem 1.5rem;
  text-align: center;
  min-width: 120px;
  backdrop-filter: blur(10px);
  position: relative;
  transition: all var(--duration) var(--ease);
}

.plan-chip:hover {
  background: rgba(255, 255, 255, 0.18);
  transform: translateY(-2px);
}

.plan-chip span {
  display: block;
  font-size: 0.8rem;
  color: rgba(255, 255, 255, 0.7);
  margin-bottom: 0.25rem;
}

.plan-chip strong {
  font-size: 1.35rem;
}

.plan-chip.popular {
  border-color: var(--gold);
  background: rgba(200, 169, 126, 0.15);
}

.plan-badge {
  position: absolute;
  top: -10px;
  left: 50%;
  transform: translateX(-50%);
  background: linear-gradient(135deg, var(--gold), var(--accent));
  color: white;
  font-size: 0.65rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  padding: 0.2rem 0.75rem;
  border-radius: 100px;
  white-space: nowrap;
}

/* ═══════════════════════════════════════════════
   CTA
   ═══════════════════════════════════════════════ */
.cta-card {
  text-align: center;
  padding: 4rem 2rem;
  background: var(--surface);
  border-radius: var(--radius-xl);
  border: 1px solid var(--border-light);
  position: relative;
  overflow: hidden;
}

.cta-decor {
  display: flex;
  justify-content: center;
  gap: 2rem;
  margin-bottom: 1.5rem;
}

.cta-star {
  color: var(--gold);
  font-size: 1.5rem;
  opacity: 0.4;
  animation: star-twinkle 3s ease-in-out infinite;
}

.cta-star:nth-child(2) { animation-delay: 1s; }
.cta-star:nth-child(3) { animation-delay: 2s; }

.cta-buttons {
  display: flex;
  justify-content: center;
  gap: 1rem;
  flex-wrap: wrap;
}

/* ═══════════════════════════════════════════════
   RESPONSIVE
   ═══════════════════════════════════════════════ */
@media (max-width: 1024px) {
  .features-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 768px) {
  .hero {
    padding: 6rem 0 3rem;
    min-height: auto;
  }

  .hero-inner {
    grid-template-columns: 1fr;
    gap: 3rem;
    text-align: center;
  }

  .hero-content {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .hero-actions {
    justify-content: center;
  }

  .hero-stats {
    justify-content: center;
  }

  .hero-visual {
    order: -1;
  }

  .phone-frame {
    width: 220px;
    height: 440px;
    border-radius: 32px;
  }

  .phone-screen {
    border-radius: 24px;
  }

  .features-grid {
    grid-template-columns: 1fr;
    gap: 1rem;
  }

  .feature-card {
    display: flex;
    text-align: left;
    gap: 1rem;
    padding: 1.5rem;
    align-items: flex-start;
  }

  .feature-icon {
    margin: 0;
    width: 56px;
    height: 56px;
    min-width: 56px;
    font-size: 1.5rem;
    border-radius: 16px;
  }

  .showcase-phone {
    width: 120px;
    height: 220px;
  }

  .languages-layout {
    grid-template-columns: 1fr;
    gap: 2.5rem;
    text-align: center;
  }

  .premium-plans {
    flex-direction: column;
  }

  .plan-chip {
    width: 100%;
  }
}

@media (max-width: 480px) {
  .hero-actions {
    flex-direction: column;
    width: 100%;
  }

  .store-btn {
    width: 100%;
    justify-content: center;
  }

  .languages-grid {
    grid-template-columns: 1fr;
  }

  .showcase-row {
    gap: 1rem;
  }

  .showcase-phone {
    width: 100px;
    height: 180px;
  }

  .cta-buttons {
    flex-direction: column;
    align-items: center;
  }
}
</style>

<template>
  <footer class="footer pattern-bg">
    <div class="container">
      <!-- Decorative divider -->
      <div class="footer-ornament">
        <svg viewBox="0 0 200 30" width="200" height="30">
          <line
            x1="0"
            y1="15"
            x2="80"
            y2="15"
            stroke="#C8A97E"
            stroke-width="1"
            opacity="0.4"
          />
          <circle
            cx="100"
            cy="15"
            r="6"
            fill="none"
            stroke="#C8A97E"
            stroke-width="1"
            opacity="0.6"
          />
          <circle cx="100" cy="15" r="2" fill="#C8A97E" opacity="0.6" />
          <line
            x1="120"
            y1="15"
            x2="200"
            y2="15"
            stroke="#C8A97E"
            stroke-width="1"
            opacity="0.4"
          />
        </svg>
      </div>

      <div class="footer-grid">
        <div class="footer-brand">
          <div class="footer-logo">
            <img src="/logo.svg" alt="NoorQuran Logo" width="40" height="40" />
            <span>NoorQuran</span>
          </div>
          <p class="footer-desc">
            Your complete Quran companion. Read, listen, and connect with the
            Holy Quran anywhere, anytime.
          </p>
          <p class="footer-arabic arabic-text">
            بِسْمِ ٱللَّٰهِ ٱلرَّحْمَٰنِ ٱلرَّحِيمِ
          </p>
        </div>

        <div class="footer-col">
          <h4>App</h4>
          <a href="#features">Features</a>
          <a href="#screenshots">Screenshots</a>
          <a href="#download">Download</a>
        </div>

        <div class="footer-col">
          <h4>Legal</h4>
          <router-link to="/privacy">Privacy Policy</router-link>
          <a href="mailto:contact@noorquran.app">Contact Us</a>
        </div>

        <div class="footer-col">
          <h4>Download</h4>
          <a
            href="https://play.google.com/store/apps/details?id=com.boubakerchieb.noorquran"
            target="_blank"
            rel="noopener"
            >Google Play</a
          >
          <a href="#" target="_blank" rel="noopener">App Store (Soon)</a>
        </div>
      </div>

      <div class="footer-bottom">
        <p>
          &copy; {{ new Date().getFullYear() }} NoorQuran. All rights reserved.
        </p>
        <p class="footer-verse arabic-text">﴿ نُورٌ عَلَىٰ نُورٍ ﴾</p>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background: linear-gradient(180deg, var(--bg) 0%, #f0ebe3 100%);
  padding: 4rem 0 2rem;
  margin-top: 0;
}

.footer-ornament {
  text-align: center;
  margin-bottom: 3rem;
}

.footer-grid {
  display: grid;
  grid-template-columns: 1.5fr 1fr 1fr 1fr;
  gap: 3rem;
  margin-bottom: 3rem;
}

.footer-brand {
  max-width: 320px;
}

.footer-logo {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  margin-bottom: 1rem;
}

.footer-logo span {
  font-size: 1.3rem;
  font-weight: 800;
  color: var(--text);
}

.footer-desc {
  font-size: 0.92rem;
  color: var(--text-secondary);
  line-height: 1.7;
  margin-bottom: 1rem;
}

.footer-arabic {
  font-size: 1.1rem;
  color: var(--gold-dark);
  opacity: 0.7;
}

.footer-col {
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
}

.footer-col h4 {
  font-size: 0.85rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.06em;
  color: var(--text);
  margin-bottom: 0.5rem;
}

.footer-col a {
  font-size: 0.92rem;
  color: var(--text-secondary);
  text-decoration: none;
  transition: color var(--duration) var(--ease);
}

.footer-col a:hover {
  color: var(--primary);
}

.footer-bottom {
  border-top: 1px solid var(--border);
  padding-top: 1.5rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.footer-bottom p {
  font-size: 0.85rem;
  color: var(--text-tertiary);
}

.footer-verse {
  font-size: 1.2rem !important;
  color: var(--gold-dark) !important;
  opacity: 0.5;
}

@media (max-width: 768px) {
  .footer-grid {
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
  }

  .footer-brand {
    grid-column: 1 / -1;
  }

  .footer-bottom {
    flex-direction: column;
    gap: 0.75rem;
    text-align: center;
  }
}

@media (max-width: 480px) {
  .footer-grid {
    grid-template-columns: 1fr;
  }
}
</style>

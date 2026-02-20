<template>
  <main class="privacy-page">
    <section class="privacy-hero pattern-bg">
      <div class="container">
        <div class="privacy-hero-content">
          <span class="section-label">Legal</span>
          <h1>Privacy Policy</h1>
          <p class="subtitle">Last updated: February 20, 2026</p>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="container">
        <div class="privacy-content">
          <div class="privacy-nav hide-mobile">
            <h4>On this page</h4>
            <a
              v-for="section in sections"
              :key="section.id"
              :href="'#' + section.id"
              :class="{ active: activeSection === section.id }"
            >
              {{ section.title }}
            </a>
          </div>

          <div class="privacy-body">
            <div class="privacy-intro card">
              <p>
                <strong>NoorQuran</strong> ("we", "our", or "us") is committed
                to protecting your privacy. This Privacy Policy explains how we
                collect, use, disclose, and safeguard your information when you
                use our mobile application NoorQuran (the "App"). Please read
                this policy carefully.
              </p>
            </div>

            <div id="information-collected" class="privacy-section reveal">
              <h2>1. Information We Collect</h2>

              <h3>1.1 Location Data</h3>
              <p>
                We request access to your device's location
                <strong>only</strong> to provide accurate prayer times based on
                your geographic position and to calculate the Qibla direction.
                Your location data is processed locally on your device and is
                sent to the Aladhan API solely to compute prayer times. We do
                not store, track, or share your precise location.
              </p>

              <h3>1.2 Device Information</h3>
              <p>
                We may collect minimal, non-personally identifiable device
                information (such as device type, operating system version, and
                app version) for the purpose of improving app performance and
                diagnosing issues.
              </p>

              <h3>1.3 In-App Purchases</h3>
              <p>
                If you subscribe to NoorQuran Premium, your purchase is
                processed entirely through the Google Play Store or Apple App
                Store. We do not collect, store, or have access to your payment
                information (credit card numbers, billing addresses, etc.).
                Transaction details are managed by Google/Apple according to
                their respective privacy policies.
              </p>

              <h3>1.4 User Preferences</h3>
              <p>
                We store your app preferences (such as selected language, theme,
                reciter choice, bookmarks, and notification settings) locally on
                your device using standard device storage. This data is not
                transmitted to any server.
              </p>
            </div>

            <div id="data-usage" class="privacy-section reveal">
              <h2>2. How We Use Your Information</h2>
              <p>We use the information we collect to:</p>
              <ul>
                <li>Display accurate prayer times for your location</li>
                <li>Calculate Qibla direction from your position</li>
                <li>Show the Hijri date</li>
                <li>Deliver prayer notifications at the correct times</li>
                <li>Save your bookmarks and reading progress locally</li>
                <li>Improve app stability and performance</li>
              </ul>
              <p>
                We do <strong>not</strong> use your data for advertising,
                marketing, profiling, or any purpose other than delivering core
                app functionality.
              </p>
            </div>

            <div id="third-party" class="privacy-section reveal">
              <h2>3. Third-Party Services</h2>
              <p>NoorQuran uses the following third-party services:</p>

              <div class="service-card">
                <h4>Aladhan API</h4>
                <p>
                  Used for prayer time calculations and Hijri date conversion.
                  Your approximate location (latitude/longitude) is sent to
                  calculate prayer times. See
                  <a
                    href="https://aladhan.com/privacy"
                    target="_blank"
                    rel="noopener"
                    >Aladhan's Privacy Policy</a
                  >.
                </p>
              </div>

              <div class="service-card">
                <h4>Al Quran Cloud API</h4>
                <p>
                  Used to fetch Quran text, translations, and audio recitations.
                  No personal data is sent with these requests.
                </p>
              </div>

              <div class="service-card">
                <h4>Google Play / Apple App Store</h4>
                <p>
                  Used for app distribution and in-app purchase processing.
                  Subject to
                  <a
                    href="https://policies.google.com/privacy"
                    target="_blank"
                    rel="noopener"
                    >Google's</a
                  >
                  and
                  <a
                    href="https://www.apple.com/legal/privacy/"
                    target="_blank"
                    rel="noopener"
                    >Apple's</a
                  >
                  respective privacy policies.
                </p>
              </div>

              <div class="service-card">
                <h4>Expo / EAS</h4>
                <p>
                  Used for app building and over-the-air updates. See
                  <a
                    href="https://expo.dev/privacy"
                    target="_blank"
                    rel="noopener"
                    >Expo's Privacy Policy</a
                  >.
                </p>
              </div>
            </div>

            <div id="data-storage" class="privacy-section reveal">
              <h2>4. Data Storage & Security</h2>
              <p>
                All user preferences, bookmarks, and app settings are stored
                <strong>locally on your device</strong>
                using AsyncStorage. We do not maintain any external database or
                server that stores your personal data.
              </p>
              <p>
                We implement reasonable technical measures to protect the
                information processed through the App. However, no method of
                electronic storage is 100% secure, and we cannot guarantee
                absolute security.
              </p>
            </div>

            <div id="notifications" class="privacy-section reveal">
              <h2>5. Push Notifications</h2>
              <p>
                NoorQuran may send local push notifications for prayer time
                reminders. These notifications are generated entirely on your
                device based on calculated prayer times. We do not use any
                external push notification service that would require
                transmitting your data to third-party servers.
              </p>
              <p>
                You can enable or disable notifications at any time through the
                app settings or your device's notification settings.
              </p>
            </div>

            <div id="children" class="privacy-section reveal">
              <h2>6. Children's Privacy</h2>
              <p>
                NoorQuran is suitable for users of all ages. We do not knowingly
                collect personal information from children under 13. The app
                does not require account creation, and no personal data is
                collected beyond what is described in this policy.
              </p>
            </div>

            <div id="your-rights" class="privacy-section reveal">
              <h2>7. Your Rights</h2>
              <p>You have the right to:</p>
              <ul>
                <li>
                  <strong>Access:</strong> All your data is stored locally on
                  your device and accessible through the app.
                </li>
                <li>
                  <strong>Delete:</strong> You can clear all app data by
                  uninstalling the app or clearing app data in your device
                  settings.
                </li>
                <li>
                  <strong>Opt-out:</strong> You can deny location permissions or
                  disable notifications at any time.
                </li>
                <li>
                  <strong>Portability:</strong> As all data is stored locally,
                  your data goes wherever your device goes.
                </li>
              </ul>
            </div>

            <div id="changes" class="privacy-section reveal">
              <h2>8. Changes to This Policy</h2>
              <p>
                We may update this Privacy Policy from time to time. We will
                notify you of any changes by updating the "Last updated" date at
                the top of this page. You are encouraged to review this Privacy
                Policy periodically.
              </p>
            </div>

            <div id="contact" class="privacy-section reveal">
              <h2>9. Contact Us</h2>
              <p>
                If you have any questions or concerns about this Privacy Policy,
                please contact us:
              </p>
              <div class="contact-card card">
                <div class="contact-item">
                  <span class="contact-icon">📧</span>
                  <div>
                    <strong>Email</strong>
                    <a href="mailto:contact@noorquran.app"
                      >contact@noorquran.app</a
                    >
                  </div>
                </div>
                <div class="contact-item">
                  <span class="contact-icon">👤</span>
                  <div>
                    <strong>Developer</strong>
                    <span>Boubaker Chieb</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const activeSection = ref("information-collected");

const sections = [
  { id: "information-collected", title: "1. Information Collected" },
  { id: "data-usage", title: "2. Data Usage" },
  { id: "third-party", title: "3. Third-Party Services" },
  { id: "data-storage", title: "4. Data Storage" },
  { id: "notifications", title: "5. Notifications" },
  { id: "children", title: "6. Children's Privacy" },
  { id: "your-rights", title: "7. Your Rights" },
  { id: "changes", title: "8. Policy Changes" },
  { id: "contact", title: "9. Contact Us" },
];

function handleScroll() {
  for (const section of [...sections].reverse()) {
    const el = document.getElementById(section.id);
    if (el && el.getBoundingClientRect().top <= 150) {
      activeSection.value = section.id;
      break;
    }
  }
}

onMounted(() => {
  window.addEventListener("scroll", handleScroll);

  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) entry.target.classList.add("visible");
      });
    },
    { threshold: 0.1 },
  );
  document.querySelectorAll(".reveal").forEach((el) => observer.observe(el));
});

onUnmounted(() => window.removeEventListener("scroll", handleScroll));
</script>

<style scoped>
.privacy-hero {
  padding: 10rem 0 4rem;
  background: linear-gradient(180deg, var(--primary-light) 0%, var(--bg) 100%);
}

.privacy-hero-content {
  max-width: 600px;
}

.privacy-hero h1 {
  margin-bottom: 0.5rem;
}

.privacy-content {
  display: grid;
  grid-template-columns: 220px 1fr;
  gap: 3rem;
  align-items: start;
}

/* Sticky sidebar nav */
.privacy-nav {
  position: sticky;
  top: 100px;
  display: flex;
  flex-direction: column;
  gap: 0.25rem;
}

.privacy-nav h4 {
  font-size: 0.8rem;
  text-transform: uppercase;
  letter-spacing: 0.06em;
  color: var(--text-tertiary);
  margin-bottom: 0.75rem;
}

.privacy-nav a {
  font-size: 0.85rem;
  color: var(--text-secondary);
  text-decoration: none;
  padding: 0.4rem 0.75rem;
  border-left: 2px solid transparent;
  border-radius: 0 6px 6px 0;
  transition: all var(--duration) var(--ease);
}

.privacy-nav a:hover {
  color: var(--primary);
  background: var(--primary-50);
}

.privacy-nav a.active {
  color: var(--primary);
  border-left-color: var(--primary);
  background: var(--primary-50);
  font-weight: 600;
}

/* Body content */
.privacy-body {
  max-width: 800px;
}

.privacy-intro {
  background: var(--primary-light);
  border-color: var(--primary-10);
  margin-bottom: 2rem;
}

.privacy-intro p {
  font-size: 1rem;
  color: var(--text-secondary);
  line-height: 1.8;
}

.privacy-section {
  margin-bottom: 3rem;
  padding-bottom: 2rem;
  border-bottom: 1px solid var(--border-light);
}

.privacy-section:last-child {
  border-bottom: none;
}

.privacy-section h2 {
  font-size: 1.5rem;
  margin-bottom: 1.25rem;
  color: var(--primary-dark);
}

.privacy-section h3 {
  font-size: 1.1rem;
  margin-top: 1.5rem;
  margin-bottom: 0.5rem;
  color: var(--text);
}

.privacy-section p {
  font-size: 0.95rem;
  color: var(--text-secondary);
  line-height: 1.8;
  margin-bottom: 0.75rem;
}

.privacy-section ul {
  list-style: none;
  padding: 0;
  margin: 1rem 0;
}

.privacy-section ul li {
  position: relative;
  padding-left: 1.5rem;
  margin-bottom: 0.75rem;
  font-size: 0.95rem;
  color: var(--text-secondary);
  line-height: 1.7;
}

.privacy-section ul li::before {
  content: "";
  position: absolute;
  left: 0;
  top: 0.65rem;
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background: var(--primary);
}

.service-card {
  background: var(--bg);
  border: 1px solid var(--border-light);
  border-radius: var(--radius-sm);
  padding: 1.25rem 1.5rem;
  margin: 1rem 0;
}

.service-card h4 {
  font-size: 1rem;
  color: var(--text);
  margin-bottom: 0.4rem;
}

.service-card p {
  font-size: 0.88rem;
  margin: 0;
}

.service-card a {
  color: var(--primary);
  text-decoration: underline;
  text-underline-offset: 2px;
}

.contact-card {
  margin-top: 1rem;
  display: flex;
  flex-direction: column;
  gap: 1.25rem;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.contact-icon {
  font-size: 1.5rem;
}

.contact-item strong {
  display: block;
  font-size: 0.85rem;
  color: var(--text-tertiary);
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.04em;
  margin-bottom: 0.15rem;
}

.contact-item a,
.contact-item span {
  font-size: 0.95rem;
  color: var(--text);
}

@media (max-width: 768px) {
  .privacy-hero {
    padding: 8rem 0 3rem;
  }

  .privacy-content {
    grid-template-columns: 1fr;
    gap: 0;
  }
}
</style>

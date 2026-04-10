<template>
  <Navbar />
  <Header />

  <router-view />

  
  <CookiesBanner />
  <WhatsAppButton />
  <PhoneButton />

  
  <div class="cookie-floating" @click="openModal">
    
  </div>

  <CookieSettingsModal v-model="showCookiesModal" />

 
  <button 
    v-if="showButton" 
    class="scroll-top-btn"  
    @click="scrollToTop"
  >
    ↑
  </button>

  <Footer />
</template>

<script>
import { ref, onMounted, onUnmounted } from 'vue'

import Header from "./components/Header.vue"
import Navbar from "./components/Navbar.vue"
import Footer from "./components/Footer.vue"

import WhatsAppButton from "./components/WhatsAppButton.vue"
import PhoneButton from "./components/PhoneButton.vue"
import CookiesBanner from "./components/CookiesBanner.vue"
import CookieSettingsModal from "./components/CookieSettingsModal.vue"

export default {
  components: {
    Header,
    Navbar,
    Footer,
    WhatsAppButton,
    PhoneButton,
    CookiesBanner,
    CookieSettingsModal
  },

  setup() {
    const showCookiesModal = ref(false)
    const showButton = ref(false)

    const openModal = () => {
      showCookiesModal.value = true
    }

    const checkScroll = () => {
      showButton.value = window.scrollY > 300
    }

    const scrollToTop = () => {
      window.scrollTo({ top: 0, behavior: 'smooth' })
    }

    onMounted(() => {
      window.addEventListener('scroll', checkScroll)
    })

    onUnmounted(() => {
      window.removeEventListener('scroll', checkScroll)
    })

    return {
      showCookiesModal,
      showButton,
      openModal,
      scrollToTop
    }
  }
}
</script>
<style scoped>


.scroll-top-btn {
  position: fixed;
  bottom: 19rem;
  right: 1.3%;
  background-color: rgb(247, 248, 248);
  color: rgb(185, 131, 50);
  border: none;
  border-radius: 50%;
  width: 55px;
  height: 55px;
  font-size: 1.5rem;
  font-weight: 800;
  cursor: pointer;
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.35);
  transition: transform 0.3s, background-color 0.3s, box-shadow 0.3s;
  z-index: 1000;
  display: flex;
  align-items: center;
  justify-content: center;
}

.scroll-top-btn:hover {
  background-color: #f5b868;
  color: #ffffff;
  transform: scale(1.15);
  box-shadow: 0 8px 20px rgba(250, 247, 247, 0.45);
}

.arrow {
  position: fixed;
  display: inline-block;
  font-weight: bold;
  font-size: 1.5rem;
  animation: float 1.5s ease-in-out infinite;
}

.cookie-floating:hover {
  transform: scale(1.12);
  background: rgba(209, 118, 13, 0.22);
  box-shadow: 0 6px 25px rgba(206, 162, 16, 0.7);
}
@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-5px); }
}
.whatsapp-btn::after,
.phone-btn::after {
  content: "";
  position: absolute;
  inset: 0;
  border-radius: 50%;
  background: rgba(255,255,255,0.2);
  opacity: 0;
  transition: 0.3s;
}

.whatsapp-btn:hover::after,
.phone-btn:hover::after {
  opacity: 1;
}
@media (max-width: 768px) {
  .scroll-top-btn {
    width: 45px;
    height: 45px;
    font-size: 18px;
    bottom: 305px;
    margin-right: 15px;
  }
}
</style>

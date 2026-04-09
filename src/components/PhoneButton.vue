<template>
  <a href="tel:+34600000000" class="phone-btn" aria-label="Teléfono">
    
    <!-- SVG teléfono -->
    <svg viewBox="0 0 24 24" fill="currentColor">
      <path d="M6.6 10.8c1.5 2.9 3.7 5.1 6.6 6.6l2.2-2.2c.3-.3.7-.4 1.1-.3 1.2.4 2.5.6 3.8.6.6 0 1 .4 1 1V21c0 .6-.4 1-1 1C10.1 22 2 13.9 2 3c0-.6.4-1 1-1h4.5c.6 0 1 .4 1 1 0 1.3.2 2.6.6 3.8.1.4 0 .8-.3 1.1l-2.2 2.1Z"/>
    </svg>

  </a>
</template>

<style scoped>
.phone-btn {
  position: fixed;
  bottom: 20px;
  left: 30px;
  width: 60px;
  height: 60px;
  border-radius: 50%;

  background: linear-gradient(45deg, #b87333, #ffd8a6);
  color: white;

  display: flex;
  align-items: center;
  justify-content: center;

  z-index: 99999;
  box-shadow: 0 10px 25px rgba(184,115,51,0.25);
  transition: all 0.3s ease;
}

/* icon */
.phone-btn svg {
  width: 24px;
  height: 24px;
}

/* hover premium */
.phone-btn:hover {
  transform: scale(1.1);
  box-shadow: 0 12px 30px rgba(184,115,51,0.5);
}
</style>
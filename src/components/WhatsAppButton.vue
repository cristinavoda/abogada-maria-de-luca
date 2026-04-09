<template>
  <a 
    href="https://wa.me/34600000000" 
    target="_blank" 
    class="whatsapp-btn"
    aria-label="WhatsApp"
  >
    <!-- SVG WhatsApp -->
    <svg viewBox="0 0 24 24" fill="currentColor">
      <path d="M20 3.5A11.9 11.9 0 0 0 12.05 1 11.94 11.94 0 0 0 2 13.06c0 2.1.55 4.16 1.6 5.97L2 23l4.1-1.57a11.9 11.9 0 0 0 5.95 1.52h.01c6.6 0 12-5.4 12-12 0-3.2-1.25-6.2-3.5-8.45ZM12.06 21a9.9 9.9 0 0 1-5.05-1.39l-.36-.21-2.44.93.93-2.38-.24-.37a9.94 9.94 0 1 1 7.16 3.42Zm5.44-7.4c-.3-.15-1.77-.87-2.04-.97-.27-.1-.46-.15-.65.15-.2.3-.75.97-.92 1.17-.17.2-.35.22-.65.07-.3-.15-1.28-.47-2.44-1.5-.9-.8-1.5-1.8-1.67-2.1-.17-.3-.02-.46.13-.6.13-.13.3-.35.45-.52.15-.17.2-.3.3-.5.1-.2.05-.37-.02-.52-.07-.15-.65-1.57-.9-2.15-.23-.55-.47-.47-.65-.48h-.55c-.2 0-.52.07-.8.37-.27.3-1.05 1.03-1.05 2.5s1.07 2.9 1.22 3.1c.15.2 2.1 3.2 5.1 4.5.7.3 1.25.48 1.67.62.7.22 1.33.19 1.83.12.56-.08 1.77-.72 2.02-1.42.25-.7.25-1.3.17-1.42-.07-.12-.27-.2-.57-.35Z"/>
    </svg>
  </a>
</template>

<style scoped>
.whatsapp-btn {
  position: fixed;
  bottom: 20px;
  right: 20px;
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background: #25D366;
  color: white;

  display: flex;
  align-items: center;
  justify-content: center;

  z-index: 99999;
  box-shadow: 0 10px 25px rgba(0,0,0,0.2);
  transition: all 0.3s ease;
}


.whatsapp-btn svg {
  width: 26px;
  height: 26px;
}


.whatsapp-btn:hover {
  transform: scale(1.1);
  box-shadow: 0 12px 30px rgba(37,211,102,0.5);
}
</style>
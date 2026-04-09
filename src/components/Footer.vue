<template>
  <footer class="footer">
    <p>© 2026 María de Luca. Todos los derechos reservados.</p>
    <p>Contacto: info@mariadeluca.com | +34 600 123 456</p>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
.footer {
  text-align: center;
  padding: 20px;
  background: #f8f8f8;
  border-top: 1px solid #ddd;
  color: #645823;
    text-shadow: wheat 1px 1px 2px, rgb(141, 115, 44) 2px 2px 4px;
  font-size: 0.9rem;
}
@media (max-width: 768px) {
  footer {
    flex-direction: column;      
    align-items: center;         
    text-align: center;          
    padding: 2rem 1rem;         
  }

  footer .footer-links {
    flex-direction: column;      
    gap: 15px;                   
    margin-bottom: 1.5rem;
  }

  footer .footer-socials {
    margin-top: 1rem;
    justify-content: center;     
  }

  footer p {
    font-size: 0.9rem;           
  }
}

@media (min-width: 769px) and (max-width: 1024px) {
  footer {
    flex-direction: row;          
    justify-content: space-between;
    padding: 2rem 3rem;
  }

  footer .footer-links {
    flex-direction: row;
    gap: 25px;
  }

  footer p {
    font-size: 1rem;
  }
}
</style>
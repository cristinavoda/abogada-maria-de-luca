<template>
  <nav class="navbar">
    <div class="logo">
      <img src="/images/logo.png" alt="María de Luca" class="logo-img" />
     
    
    </div>
    <ul :class="{ 'nav-links': true, 'open': openMenu }">
  <li>
    <router-link to="/" @click="closeMenu">Inicio</router-link>
  </li>
  <li>
    <router-link to="/sobre" @click="closeMenu">Areas de actividad</router-link>
  </li>
  <li>
    <router-link to="/servicios" @click="closeMenu">Servicios</router-link>
  </li>
  <li>
    <router-link to="/contacto" @click="closeMenu">Contacto</router-link>
  </li>
</ul>
    <div class="burger" @click="toggleMenu">
      <div></div><div></div><div></div>
    </div>
  </nav>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const openMenu = ref(false);
    const toggleMenu = () => { openMenu.value = !openMenu.value; };
     const closeMenu = () => { openMenu.value = false; };
    return { openMenu, toggleMenu, closeMenu};
  }
};
</script>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  
  padding:20px 40px;
  backdrop-filter: blur(10px);
  background: rgba(255,255,255,0.15);
  position: sticky;
  top: 0;
  z-index: 1000;
}

.logo {
  font-weight: 700;
  font-size: 1.5rem;
  margin: 0;
  font-family: Robo slab;
  color: rgb(141, 115, 44);
  font-weight: 500;
  text-shadow: wheat 1px 1px 2px, rgb(141, 115, 44) 2px 2px 4px;
}

.logo-img {
  height: 50px;
  object-fit: contain;
  transition: 0.3s ease;
   filter: drop-shadow(2px 2px 6px rgba(0,0,0,0.2));
}


.logo-img:hover {
  transform: scale(1.05);
  filter: drop-shadow(0 4px 10px rgba(184,115,51,0.3));
}
.nav-links {
  display: flex;
  margin-top: 0;
  list-style: none;
  gap: 40px;
  justify-content: center;
   color: #705509;
}

.nav-links li a {
  text-decoration: none;
  font-size: 1.3rem;
  font-weight: 500;
  transition: 0.3s;
  color: #a56b15;
   text-shadow: rgb(228, 205, 161) 1px 1px 2px, rgb(141, 115, 44) 2px 2px 4px;
}

.nav-links li a:hover {
  color: #b87333;
}


.burger {
  display: none;
  flex-direction: column;
  cursor: pointer;
  gap: 5px;
}

.burger div {
  width: 25px;
  height: 3px;
    background-color: #b66c27;
    text-shadow: #1f1e1d 3px 4px 2px;
}


@media (max-width: 768px) {
  .nav-links {
    position: fixed;
    top: 0;
    left: 0;
    height: 100vh;
    width: 100%;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: rgba(255,255,255,0.95);
    transform: translateX(-100%);
    transition: 0.5s;
    z-index: 1001;
  }
  .nav-links.open { transform: translateX(0); }
  .burger { display: flex; }
}
</style>
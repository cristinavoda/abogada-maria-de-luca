<template>
  <div class="home">
    <div class="bg-layer"></div>  
    <div class="content-layer">   
 <Header />
    <section class="hero">
   <h1 class="gradient-cobre sparkle">Defendiendo tus derechos con rigor y cercanía</h1>   
  
  <p>
    Asesoramiento legal en derecho civil y mercantil con un enfoque
    personalizado y profesional.
  </p>
  <router-link to="/contacto" class="btn">Solicitar consulta</router-link>
</section>

    <section class="servicios">
      <h2>Servicios destacados</h2>
      <div class="cards">
        <div class="card">
          <h3>Derecho Civil</h3>
          <p>Asesoramiento en contratos, herencias y más.</p>
           <router-link to="/servicios" class="btn">Ver servicios</router-link>
        </div>
        <div class="card">
          <h3>Derecho Mercantil</h3>
          <p>Ayuda legal para empresas y autónomos.</p>
          <router-link to="/servicios" class="btn">Ver servicios</router-link>
        </div>
      </div>
    </section>
 <Footer />
    </div>
      
  </div>
   
</template>

<script>
import Header from "../components/Header.vue";
import Footer from "../components/Footer.vue";




export default {
  name: "Home",
  components: { Header, Footer,},
};

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Robo+Slab:wght@400;700&display=swap');

h1, h2, h3 {
  font-family: 'Robo Slab', serif;
  font-weight: 700;
}


.gradient-cobre {
  background: linear-gradient(45deg, #6d5024, #ffd8a6);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  color: transparent;
  display: inline-block;
}


.sparkle {
  position: relative;
  animation: sparkleAnim 2s infinite;
}

@keyframes sparkleAnim {
  0%, 100% { text-shadow: 0 0 2px #88710a; }
  50% { text-shadow: 0 0 8px #ffd8a6; }
}
.home {
  position: relative;
  width: 100%;
  min-height: 100vh;
  overflow: hidden;
}


.bg-layer {
  position: fixed;
  top: 0; left: 5%; right: 1%; bottom: 0;
  width: 100%;
  height: 100%;
  background: url('/images/oficina.png') center/cover no-repeat;
  z-index: 0;
}
@keyframes zoomInBg {
  0% { transform: scale(1); }
  100% { transform: scale(1.35); }
}



.content-layer {
  position: relative;
  z-index: 1;
  backdrop-filter: blur(5px); 
  padding: 40px 20px;
}
.hero {
  text-align: center;
  padding: 120px 20px;
  
   z-index: 1;
  backdrop-filter: blur(5px); 
  background: rgba(255, 255, 255, 0.2); 
}


.hero h1 {
  font-size: 1.8rem;
  max-width: 700px;
  margin: auto;
  line-height: 1.3;
}

.hero p {
  margin-top: 20px;
  font-size: 1.2rem;
  color: #705509;
}
.servicios h2 {
  font-size: 1.5rem;
  margin-bottom: 20px;
  color: #705509;}

.btn {
  display: inline-block;
  margin-top: 30px;
  font-family: 'Roboto Slab', serif;
  font-weight: 600;
  padding: 14px 28px;
  background: transparent;
  color: #705509;
  border-bottom: 2px solid #705509;
  border-radius: 18px;
  transition: 0.3s;
}

.btn:hover {
  background: transparent;
}

.hero p {
  font-size: 1.2rem;
  margin-bottom: 30px;
}


.servicios {
  padding: 50px 20px;
  text-align: center;
}

.cards {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
  margin-top: 30px;
}

.card {
   z-index: 1;
  backdrop-filter: blur(5px); 
  background: rgba(255, 255, 255, 0.2); 
  padding: 20px;
  border-radius: 8px;
  width: 390px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}

.card h3 {
  margin-bottom: 10px;
  color: #5e4a20;
}
</style>
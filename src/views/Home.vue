<template>
  <section id="home">
    <div class="home">
    
      <div class="bg-layer"></div>  

      
      <div class="content-layer"> 
        <Header />

        <section class="hero">
          <h1 class="gradient-cobre sparkle">
            Defendiendo tus derechos con rigor y cercanía
          </h1>   
          <p>
            Asesoramiento legal en derecho civil y mercantil con un enfoque
            personalizado y profesional.
          </p>
          <p>
           Mi compromiso es ofrecerte un apoyo integral en la gestión de cualquier conflicto en el ámbito civil y de familia, así como un acompañamiento cercano y especializado en inmobiliario, procedimientos Penales, Violencia de Género, Jurisdicción de Menores, ley de la segunda oportunidad y función pública.
          </p>
          <p> El Derecho Civil es la rama que más aspectos de la vida cotidiana abarca. Prácticamente todo el día a día de las personas es derecho civil: relaciones familiares, sucesión, patrimonio de la persona, obligaciones y contratos, responsabilidad contractual y extracontractual. Se dice que es la contraposición al Derecho administrativo, ya que es un derecho puramente privado, en el que la administración no interviene para nada.

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
      </div>
    </div>
  </section>

 
  <section id="sobre" class="sobre">
  
    <div class="sobre-content">
       <h1 class="sobre-title">Sobre María de Luca</h1>
      <img src="/images/maria.png" alt="María de Luca" class="sobre-float-img" />
      <div class="sobre-text">
      <p>
        Abogada especializada en derecho civil y mercantil con más de X años de experiencia. El Derecho Civil regula las relaciones entre personas, lo que firmamos, lo que compramos, dónde vivimos y qué dejamos a los nuestros.
      </p>

      <p>
        A veces surgen conflictos que nos quitan el sueño: un inquilino que deja de pagar, una herencia que bloquea a la familia, una deuda que no logras cobrar o un banco que abusó de tu confianza.
      </p>

      <h3>Áreas de actuación:</h3>
      <ul>
        <li>Arrendamientos y Desahucios</li>
        <li>Reclamaciones de cantidad</li>
        <li>Sucesiones y Herencias</li>
        <li>Gastos Hipotecarios y Cláusulas Abusivas</li>
      </ul>
 <p>
        Abogada especializada en derecho civil y mercantil con más de X años de experiencia. El Derecho Civil es, en realidad, el derecho de la vida diaria. Regula las relaciones entre personas, lo que firmamos, lo que compramos, dónde vivimos y qué dejamos a los nuestros cuando ya no estamos.
      </p>

      <p>
        A veces, esas relaciones se rompen o surgen conflictos que nos quitan el sueño. Un inquilino que deja de pagar, una herencia que bloquea a la familia, una deuda que no logras cobrar o un banco que abusó de tu confianza.
      </p>

      
      
      
      <p>
        ¿En qué podemos ayudarte? Áreas de actuación: No somos un despacho generalista que «hace de todo un poco». Nos centramos en proteger tu patrimonio y tus derechos en estas cuatro áreas clave:
      </p>

      <h3>1. Arrendamientos y Desahucios: Protege tu propiedad</h3>
      <p>
        El mercado del alquiler en Lleida genera muchas dudas tanto a propietarios como a inquilinos. Un contrato mal redactado es la semilla de un futuro problema.
      </p>

      <ul>
        <li>Redacción de Contratos: No uses modelos genéricos de internet. Redactamos contratos de arrendamiento blindados.</li>
        <li>Desahucios y Reclamación de Rentas: Iniciamos el proceso de desahucio para que recuperes tu vivienda o local comercial.</li>
        <li>Conflictos Inmobiliarios: Mediamos o actuamos contundentemente según sea necesario.</li>
      </ul>

      <h3>2. Reclamaciones de cantidad</h3>
      <p>
        Gestionamos reclamaciones de cantidad para particulares y empresas: facturas impagadas, devoluciones de préstamos, daños y perjuicios, procedimientos monitorios.
      </p>

      <h3>3. Sucesiones y Herencias</h3>
      <p>
        Nos ocupamos de todo el proceso sucesorio, aplicando el Código Civil y Derecho Civil Catalán. Tramitación, impuestos y mediación de conflictos hereditarios.
      </p>

      <h3>4. Gastos Hipotecarios y Cláusulas Abusivas</h3>
      <p>
        Recupera tu dinero si tu hipoteca fue antes de junio 2019. Reclamación de gastos indebidos y revisión de escrituras.
      </p>

      <p>
        Hablamos claro y te mostramos la viabilidad de cualquier pleito antes de iniciarlo. Honestidad ante todo.
      </p>
     </div>
    </div>
  </section>

  
  <section class="contact-form">
    <h2>Contacto</h2>
    <form @submit.prevent="handleSubmit">
      <label>
        Nombre:
        <input type="text" v-model="form.nombre" required />
      </label>

      <label>
        Email:
        <input type="email" v-model="form.email" required />
      </label>

      <label>
        Mensaje:
        <textarea v-model="form.mensaje" rows="5" required></textarea>
      </label>

      <button type="submit">Enviar</button>
    </form>
    <p v-if="enviado" class="success-msg">¡Gracias! Tu mensaje ha sido enviado.</p>
  </section>
<div class="card-ubication" data-aos="fade-up" data-aos-delay="500" position="relative" z-index="1">
    
        <h2> Ubicación</h2>
        <div class="map-container">
        <iframe
  width="100%"
  height="350"
  style="border:0; border-radius: 12px;"
  loading="lazy"
  allowfullscreen
  referrerpolicy="no-referrer-when-downgrade"
  src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2985.037566902099!2d0.7984!3d41.6300!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x12a6a7b692cf2a05%3A0x93bf9f0f7e2e76cc!2sCarrer%20Sant%20Miquel%2C%2012%2C%2025254%20Bell-lloc%20d'Urgell%2C%20Lleida!5e0!3m2!1ses!2ses!4v1731589912345"
>
</iframe>
</div>
      </div>
  <Footer />
</template>

<script>
import Header from "../components/Header.vue";
import Footer from "../components/Footer.vue";
const scrollToSection = (id) => {
  document.getElementById(id).scrollIntoView({ behavior: "smooth" });
}



export default {
  name: "Home",
  components: { Header, Footer,},

  name: "ContactForm",
  data() {
    return {
      form: {
        nombre: "",
        email: "",
        mensaje: "",
      },
      enviado: false,
    };
  },
  methods: {
    handleSubmit() {
      console.log("Formulario enviado:", this.form);
      this.enviado = true;
      // Reinicia el formulario
      this.form.nombre = "";
      this.form.email = "";
      this.form.mensaje = "";
    },
  },
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
  top: 0; left: 0; right: 10px; bottom: 0;
  max-width: 100%;
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
  width: 100%;
  height: 100%;
  backdrop-filter: blur(5px); 
  padding: 20px 20px;
   justify-content: center;
}
.hero {
  position: relative;
   z-index: 1;
   background: rgba(255, 255, 255, 0.9); 
   backdrop-filter: blur(10px); 
  border-radius: 12px;
   margin: 1rem 0rem;
   max-width: 1800px;
  text-align: center;
  padding: 20px 20px;
  z-index: 1;
  margin-top: 60px;
  backdrop-filter: blur(15px); 
  background: rgba(243, 243, 236, 0.9); 
   justify-content: center;
  align-items: center;
  
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
  font-weight: 600;
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
  padding: 20px 20px;
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
  background: rgba(228, 226, 226, 6.993); 
  padding: 20px;
  border-radius: 8px;
  width: 390px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}

.card h3 {
  margin-bottom: 10px;
  color: #b8820d;
}
.sobre {
  max-width: 1000px;
    margin: 0 auto;
  margin: 10px auto;
  padding: 40px 40px;
  z-index: 1;
}


.sobre-title {
  font-family: 'Robo Slab', serif;
  color: #b87333; 
  text-align: center;
  margin-bottom: 40px;
  z-index: 1;
}


.sobre-content {
  display: block; 
  position: relative;
  background: rgba(255, 255, 255, 1.55);
   backdrop-filter: blur(17px); 
   padding: 40px 20px;
}

.sobre-content::after {
  content: "";
  display: block;
  clear: both; 
}

.sobre-content p,
.sobre-content ul,
.sobre-content h3 {
  line-height: 1.8;
  margin-bottom: 20px;
  list-style: none;
  font-size: 1rem;
  z-index: 1;
  
   
}
.sobre-content h3 {
  font-size: 1.2rem;
  color: #ac733d;
  font-family: Robo slab;
}

.sobre-float-img {
  float: left;
  max-width: 400px;
  border-radius: 396px;
  margin-left: 20px;
  margin-bottom: 10px;
  padding: 2px;
  background: linear-gradient(135deg, #b87333, #f5d3a1);
  opacity: 0;
  transform: scale(0.95);
  animation: fadeZoom 0.8s forwards;
  box-shadow: 
    0 10px 25px rgba(184,115,51,0.25),
    0 2px 15px rgba(184,115,51,0.2);

  border: 2px solid #fff;
  outline: 2px solid #f1d8c0;
  outline-offset: 6px;
}


@keyframes fadeZoom {
  to {
    opacity: 1;
    transform: scale(1);
  }
}


.sobre-content ul li {
  margin-bottom: 10px;
  padding-left: 0;
  color: #5e4a20; 
  z-index: 1;
}


@media (max-width: 768px) {
  .sobre {
    width: 90%;
    
    
  }
  .sobre-h1 {
    font-size: 1.5rem;
    margin-bottom: 40px;
  }
  .sobre-float-img {
    float: none;
    display: block;
    width: 40%;
    height: 100%;
     margin-top: 10px;
  }

  .sobre-content {
    width: 100%;
    height: auto;
    padding: 40px 10px 0 10px;

  }
}
.contact-form {
  max-width: 900px;
  width: 90%;
  margin: 1rem; 
  position: relative;
  z-index: 1;

  backdrop-filter: blur(16px);
  background: rgba(250, 249, 249, 0.25);

  padding: 3rem 2rem;
  border-radius: 14px;

  box-shadow: 0 10px 30px rgba(184,115,51,0.15);
  margin-bottom: 40px;
}


.contact-form h2 {
  text-align: center;
  margin-bottom: 40px;
  color: #a56b15;
  text-shadow: rgb(109, 99, 80) 1px 1px 1px, rgb(167, 139, 63) 2px 2px 4px;
  font-family: 'Roboto Slab', serif;
  font-size: 1.5rem;
  font-weight: 500;
}

label {
  display: block;
  margin-bottom: 15px;
  font-weight: 500;
  color: #805905;
  text-shadow: rgb(141, 115, 44) 2px 2px 4px;
}

input, textarea {
  width: 50%;
   font-family: 'Roboto Slab', serif;
  padding: 10px;
  margin-top: 5px;
  border: 0.1px solid #f8f4f4;
  border-bottom-color: #aca05e;
  border-radius: 5px;
   z-index: 1;
  backdrop-filter: blur(5px); 
  background: rgba(255, 255, 255, 0.2); 
  
  border-radius: 10px;
  box-shadow: 4px 2px 6px rgba(202, 125, 24, 0.1);
}

button {
  display: block;
  width: 100%;
  padding: 12px;
  font-weight: bold;
  border: none;
  border-radius: 5px;
  cursor: pointer;
   display: inline-block;
  margin-top: 30px;
  font-family: 'Roboto Slab', serif;
  font-size: 1.1rem;
  font-weight: 600;
  padding: 14px 18px;
  background: transparent;
  color: #ac670d;
  border-bottom: 3px solid #c27d22;
  width: 40%;
  border-radius: 18px;
  transition: 0.3s;
}

button:hover {
  background: #615002;
  
  backdrop-filter: blur(6px);
  background: rgba(255, 255, 255, 0.25);
}

.success-msg {
  text-align: center;
  margin-top: 15px;
  color: green;
  font-weight: bold;
}
.card-ubication {
  position: relative;
  z-index: 1;
  background-color: #faf9f2;
}
.card-ubication h2 {
  text-align: center;
  margin-top: 20px;
  margin-bottom: 20px;
  color: #bd7d06;
  font-family: 'Robo Slab', serif;

  font-size: 1.7rem;}
.card-ubication {
  position: relative;
  z-index: 1;
}
  
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
    margin-bottom: 0-2rem; 
    position: relative;       
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
    padding: 1rem 1rem;
    margin-top: 40px;
   position: relative;
   z-index: 2;
    
  }

  footer .footer-links {
    flex-direction: row;
    gap: 25px;
  }

  footer p {
    font-size: 1rem;
  }
}
@media (min-width: 1025px) {
  footer {
    display: flex;
    justify-content: space-between;
    padding: 0.5rem 0.2rem;
    margin-top: 40px;
   position: relative;
  }
}
@media (max-height: 800px) {
  .contact-wrapper {
    padding-top: 0;
    align-items: flex-start;
  }
  .contact-form {
  margin-bottom: 10px;
}
button {
  width: 40%;
   margin-bottom: 2%;
   margin-top: 10px;
}}
@media (max-width: 768px) {
 
  .bg-layer .logo {
    display: none;
  }
.sobre {
    width: 100%;
    height: fit-content;
    padding: 0 0 0 0px;
    display: inline-block;
  }
  
  .contact-wrapper {
    flex-direction: column;
    align-items: center; 
    padding: 2rem 0.1rem 1rem;
  }

 
  .contact-form {
    width: 100%;
    max-width: 100%; 
    padding: 0.1rem 1rem; 
  }
  .contact-form h2 {
  text-align: center;
  margin-bottom: 50px;
  margin-top: 20px;
  color: #a56b15;
  text-shadow: rgb(109, 99, 80) 1px 1px 1px, rgb(167, 139, 63) 2px 2px 4px;
  font-family: 'Roboto Slab', serif;
  font-size: 1.5rem;
  font-weight: 500;
}
.contact-form {
  max-width: 500px;
  align-items: flex-start;
  margin: 10px 0;
  height: auto;
  position: relative;
  z-index: 1;
  backdrop-filter: blur(8px); 
  background: rgba(255, 255, 255, 0.2); 
  padding: 3rem 2rem;
  border-radius: 10px;
  box-shadow: 4px 2px 6px rgba(202, 125, 24, 0.1);
}
@media (max-width: 768px) {
  .hero {
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-left: -40px;
  }

  .hero h1 {
    font-size: 1.8rem;
  }

  .hero p {
    font-size: 1rem;
    max-width: 90%;
  }

  .hero .btn {
    margin-top: 15px;
  }
  
.servicios {
  padding: 20px 20px;
  text-align: center;
}

.cards {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
  margin-top: 30px;
  padding: 0 10px;
  margin-left: -60px;
}

.card {
   z-index: 1;
  backdrop-filter: blur(5px); 
  background: rgba(236, 234, 234, 0.9); 
  padding: 20px;
  border-radius: 8px;
  width: 390px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}

.card h3 {
  margin-bottom: 10px;
  color: #5e4a20;
}
}
}
</style>
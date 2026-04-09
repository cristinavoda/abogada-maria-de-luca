<template>
    <div class="bg-layer">
    
      <div class="contact-wrapper">
         <div class="logo">
      <h1 ref="mainTitle" class="gradient-cobre sparkle title-shine">
  María de Luca  
</h1>
      <p>Abogada · Derecho Civil y Mercantil</p>
    </div>
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
  </div></div> 
</template>

<script>
export default {
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
body {
  overflow-x: hidden;
  overflow-y: auto;
}
.bg-layer {
  position: fixed;
  top: 0; left: 0;
  width: 100%;
  min-height: 100vh;
  background: url('/images/background.png') center/cover no-repeat;
  z-index: 0;
}
@keyframes zoomInBg {
  0% { transform: scale(1); }
  100% { transform: scale(1.35); }
}
.logo h1 {
  margin-top: 7rem;
  font-size: 2.5rem;
  color: #1d1d1f;
  font-family: Robo slab;
  color: rgb(211, 138, 29);
  font-weight: 500;
  text-shadow: rgb(109, 99, 80) 1px 1px 1px, rgb(167, 139, 63) 2px 2px 4px;
}

.logo p {
  margin-top: 10px;
  color: #41403d;
   text-shadow: rgb(209, 148, 34) 1px 1px 2px, rgb(167, 148, 99) 2px 2px 4px;
}
.contact-wrapper {
  display: flex;
  justify-content: center;
  align-items:flex-start;
  min-height: 100vh; 
  padding: 20px;
}

.contact-form {
  max-width: 900px;
  width: 100%;
  margin: 6rem; 
  position: relative;
  z-index: 1;

  backdrop-filter: blur(6px);
  background: rgba(255, 255, 255, 0.25);

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
  max-width: 900px;
  align-items: flex-start;
  margin: -10px 0;
  height: auto;
  position: relative;
  z-index: 1;
  backdrop-filter: blur(8px); 
  background: rgba(255, 255, 255, 0.2); 
  padding: 3rem 2rem;
  border-radius: 10px;
  box-shadow: 4px 2px 6px rgba(202, 125, 24, 0.1);
}

}
</style>
<template>
  <div>
  
    <section class="servicios">
      <h1>Servicios</h1>
      <div class="cards">
        <ServicioCard titulo="Derecho Civil" descripcion="Accidentes de tráfico, reclamaciones por cláusula suelo y gastos hipotecarios, IRPH, tarjetas revolving, participaciones preferentes y cláusulas abusivas.Contratos, herencias.Derecho de Personas: Estado civil, capacidad, derechos de imagen.
Derecho de Familia: Matrimonio, filiación, patria potestad, divorcio.
Derecho de Bienes/Derechos Reales: Propiedad, posesión.
Derecho de Obligaciones y Contratos: Compraventa, arrendamientos, responsabilidad civil.
Derecho de Sucesiones: Herencias y testamentos."/>
        <ServicioCard titulo="Derecho Mercantil" descripcion="Asesoramiento a empresas-Derecho de Sociedades: Constitución, funcionamiento y extinción de empresas.
Contratos Mercantiles: Compraventas, franquicias, leasing, seguros, etc..
Títulos-valor: Cheques, pagarés, letras de cambio.
Propiedad Industrial: Marcas, patentes y diseños.
Derecho Concursal: Regulación de insolvencias y quiebras.
Derecho de la Competencia: Defensa de la libre competencia y regulación de la competencia desleal."/>
        <ServicioCard titulo="Consultoría Legal" descripcion="Orientación legal personalizada , brindar la información y el asesoramiento necesarios para la resolución de cuestiones que vengan referidas a la aplicación de leyes, normativas y reglamentos en cualquier rama del Derecho, sean de ámbito internacional, estatal, autonómico o local."/>
      </div>
    </section>
      <section class="servicios-procesal">
    <h1>Derecho Procesal Civil</h1>
    <p class="intro">
      La calidad de nuestro trabajo va acompañada del servicio integral que ofrecemos a profesionales de todo tipo de sectores. Con nosotros tendrá una atención individualizada y le acompañaremos durante los procesos judiciales.
    </p>

    
   
    <h2>Alcance de los servicios y ámbito de actuación</h2>
    
    <ul>
      <li><strong>Recobro de deudas</strong> y falta de pago de rentas de alquiler.</li>
      <li><strong>Derecho de familia</strong> (separaciones, divorcios, medidas paternofiliales, régimen económico matrimonial).</li>
      <li><strong>Responsabilidad de administradores</strong>.</li>
      <li><strong>Incumplimientos contractuales</strong> (servicios, compraventa, suministros, etc.).</li>
      <li><strong>Herencias</strong>.</li>
      <li><strong>Conflictos societarios</strong>: impugnación de acuerdos sociales, separación y exclusión de socios, censura de la gestión societaria.</li>
      <li><strong>Incumplimientos de contratos mercantiles</strong>.</li>
      <li><strong>Reclamaciones frente a aseguradoras</strong> por responsabilidad civil contractual y extracontractual.</li>
      <li><strong>Expedientes de dominio</strong> y acciones de recuperación de la posesión.</li>
      <li><strong>Derechos honoríficos</strong> de la persona.</li>
      <li><strong>Reclamaciones por responsabilidad civil</strong> derivada de accidentes de tráfico.</li>
      <li><strong>Reclamaciones por responsabilidad civil</strong> derivada de accidentes de trabajo.</li>
    </ul>
  <div class="img-container">
      <img src="/images/oficina.png" alt="María de Luca" class="img" /></div>
    <p>
      Actuar correctamente ante los tribunales requiere de una alta preparación procesal y amplios conocimientos técnicos sobre el derecho para la correcta defensa de sus intereses.
    </p>

    <p>
      El conocimiento y seguimiento de su caso es de vital importancia para saber cómo actuar en el juzgado y que el caso se resuelva a nuestro favor.
    </p>

    <p>
      El abogado de Derecho Procesal Civil es fundamental para garantizar la adecuada defensa de los derechos de los ciudadanos en el ámbito judicial. Su labor abarca desde la asesoría legal hasta la representación en juicios, siendo esencial en diversas áreas del derecho.
    </p>

    <p>
      Su experiencia y conocimiento técnico son claves para obtener resultados favorables en cada caso.
    </p>
  </section>
  </div>
   
</template>

<script>
import Header from "../components/Header.vue";
import Footer from "../components/Footer.vue";
import ServicioCard from "../components/ServicioCard.vue";

export default {
  components: { Header, Footer, ServicioCard },
};
</script>

<style scoped>
.servicios h1 {
  font-size: 1.8rem;
  font-family: Robo slab;;
  text-align: center;
  margin-top: 10px;
  margin-bottom: 30px;
  background: linear-gradient(45deg, #b87333, #ffd8a6);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  }
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
   padding: 10px 10px;
   justify-content: center;
    max-width: 1500px;
  margin: 0 auto; 
}
.cards .card {
  background: white #ffd8a6;
  padding: 2rem 1.5rem 1.5rem 1.5rem;
  border-radius: 12px;
  width: 90%;
  transition: 0.3s;
  box-shadow: 3px 4px 12px rgba(0,0,0,0.05);
}
.cards .card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0,0,0,0.1);
}
.card h3 {
  margin-bottom: 10px;
  background: linear-gradient(45deg, #b87333, #ffd8a6);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.servicios-procesal {
  max-width: 1100px;
  margin: 0 auto;
  padding: 60px 20px;
  font-family: 'Robo Slab', serif;
  color: #1d1d1f;
}

.servicios-procesal h1 {
  font-size: 1.8rem;
  text-align: center;
  margin-bottom: 20px;
  background: linear-gradient(45deg, #b87333, #ffd8a6);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.servicios-procesal h2 {
  font-size: 2rem;
  margin-top: 40px;
  margin-bottom: 20px;
  color: #ac733d;
  font-family: Robo slab;
  z-index: 1;
}

.servicios-procesal p {
  line-height: 1.8;
  margin-bottom: 20px;
  font-size: 1.1rem;
   text-align: left; 
}

.servicios-procesal ul {
  list-style: none;
  padding-left: 20px;
  margin-bottom: 20px;
}

.servicios-procesal li {
  margin-bottom: 10px;
   line-height: 1.9;
   margin-right: 5px;
   text-align: left; 
}
.servicios-procesal li strong {
  color: #ac733d;
  font-weight: 600;
   display: inline-block;
  margin-right: 5px;
}
h3 {
  margin-bottom: 10px;
  background: linear-gradient(45deg, #b87333, #ffd8a6);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.img {
  width: 100%;
  max-width: 780px;
  height: auto;
  padding: 1rem;
  object-fit: cover;
  margin-bottom: 1rem;
 box-shadow: 10px 10px 30px rgba(197, 133, 14, 0.75);
  transition: transform 0.4s ease, box-shadow 0.4s ease;
  opacity: 0;
  transform: translateY(20px);
  animation: fadeInUp 0.8s ease forwards;
}

@keyframes fadeInUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
.img:hover {
  transform: translateY(-6px) scale(1.02);
  box-shadow: 0 18px 45px rgba(0, 0, 0, 0.25);
}
@media (max-width: 768px) {
  .servicios-procesal {
    padding: 20px;
  }
   .img {
    max-width: 300px;
    
}
}
</style>
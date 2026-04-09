<template>
  <section class="sobre">
    <h1 class="sobre-title">Sobre María de Luca</h1>

    <div class="sobre-content">
      <img src="/images/maria.png" alt="María de Luca" class="sobre-float-img" />

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
  </section>
</template>

<style>

.sobre {
  max-width: 1000px;
  margin: 0 auto;
  padding: 60px 20px;
}


.sobre-title {
  font-family: 'Robo Slab', serif;
  color: #b87333; 
  text-align: center;
  margin-bottom: 40px;
}


.sobre-content {
  display: block; 
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
}
.sobre-content h3 {
  font-size: 1.2rem;
  color: #ac733d;
  font-family: Robo slab;}

.sobre-float-img {
  float: right;
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
}


@media (max-width: 768px) {
  .sobre-float-img {
    float: none;
    display: block;
    margin: 0 auto 20px;
    width: 80%;
  }

  .sobre-content {
    padding: 0 10px;
  }
}
</style>
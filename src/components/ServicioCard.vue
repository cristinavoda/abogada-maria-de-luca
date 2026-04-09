<template>
  <div class="card">
    <div class="icon">⚖️</div>

    <h3 class="titulo">{{ titulo }}</h3>

    <p class="descripcion">{{ descripcion }}</p>
  </div>
</template>

<script>
export default {
  name: "ServicioCard",
  props: {
    titulo: String,
    descripcion: String,
  },
};
</script>

<style scoped>
.card {
  background: rgba(255, 255, 255, 0.9);
  padding: 30px 25px;
  border-radius: 18px;
  width: 100%;
  text-align: center;
  transition: all 0.35s ease;
  box-shadow: 0 6px 20px rgba(0,0,0,0.08);
  backdrop-filter: blur(8px);
  position: relative;
  overflow: hidden;
}


.card::before {
  content: "";
  position: absolute;
  inset: 0;
  background: linear-gradient(120deg, transparent, rgba(184,115,51,0.2), transparent);
  opacity: 0;
  transition: 0.4s;
}


.card:hover {
  transform: translateY(-8px) scale(1.02);
  box-shadow: 0 15px 35px rgba(0,0,0,0.15);
}

.card:hover::before {
  opacity: 1;
}


.icon {
  font-size: 2rem;
  margin-bottom: 15px;
  color: #b87333;
}


.titulo {
  font-size: 1.4rem;
  margin-bottom: 12px;
  background: linear-gradient(45deg, #b87333, #ffd8a6);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}


.descripcion {
  font-size: 1rem;
  color: #555;
  line-height: 1.6;
}


.card {
  opacity: 0;
  transform: translateY(20px);
  animation: fadeUp 0.8s forwards;
}

@keyframes fadeUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}


@media (max-width: 768px) {
  .card {
    padding: 25px 20px;
  }

  .titulo {
    font-size: 1.2rem;
  }
  .icon {
    font-size: 1.8rem;
    color: #b87333;
  }
}
</style>
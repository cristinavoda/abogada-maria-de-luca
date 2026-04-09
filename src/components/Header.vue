<template>
  <header class="header">
    <div class="logo">
      <h1 ref="mainTitle" class="gradient-cobre sparkle title-shine">
  María de Luca  
</h1>
      <p>Abogada · Derecho Civil y Mercantil</p>
    </div>
  </header>
</template>

<script>

export default {
  name: "Header",
};

</script>

<style scoped>
.header {
  text-align: center;
  padding: 0 0px 0px;
}

.logo h1 {
  margin: 0;
  font-size: 2.5rem;
  color: #1d1d1f;
  font-family: Robo slab;
  color: #b87333;
  font-weight: 500;
  text-shadow: rgb(173, 116, 8) 1px 1px 2px, rgb(141, 115, 44) 2px 2px 4px;
}

.logo p {
  margin-top: 10px;
  color: #41403d;
   text-shadow: rgb(209, 148, 34) 1px 1px 2px, rgb(167, 148, 99) 2px 2px 4px;
}

</style>
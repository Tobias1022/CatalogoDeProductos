<template>
  <div class="col-md-4 mb-3">
    <div class="card">
      <img :src="producto.imagen" class="card-img-top" :alt="producto.nombre">
      <div class="card-body">
        <h5 class="card-title">{{ producto.nombre }}</h5>
        <p class="card-text">{{ producto.descripcion }}</p>
        <p class="card-text"><strong>Precio: ${{ producto.precio }}</strong></p>
      </div>
    </div>

</div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>

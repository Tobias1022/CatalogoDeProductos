<template>
  <div class="container mt-5 bg-light py-4 rounded">
    <div class="row">
      <div class="col-md-4 mb-4" v-for="producto in productos" :key="producto.id">
        <div class="card">
          <img :src="producto.thumbnail" class="card-img-top" :alt="producto.name">
          <div class="card-body">
            <h5 class="card-title">{{ producto.name }}</h5>
            <p class="card-text">{{ producto.description }}</p>
            <p class="card-text"><strong>${{ producto.price }}</strong></p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
/* eslint-disable */
export default {
  name:'Producto2',
  data() {
    return {
      productos: []  
    };
  },
  mounted() {
    fetch('https://dummyjson.com/products')
      .then(response => response.json())
      .then(data => {
        this.productos = data.products; 
      })
      .catch(error => console.error('Error fetching products:', error));
  }
}
</script>

<style scoped>

</style>


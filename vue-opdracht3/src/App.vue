<script>
export default {
  data() {
    return {
      product: "",
      products: []
    };
  },
  methods: {
    addProduct() {
      this.products.push(this.product)
      this.product = '';
    }
  }
}
</script>

<template>
  <div id="app">
    <div>
      <label for="product">Product</label>
      <input type="text" id="product" v-model="product" />
      <button v-on:click="addProduct">Voeg dit product toe</button>
    </div>
    <ul>
      <li v-for="item in products" :key="item">{{ item }}</li>
    </ul>
  </div>
</template>

<style>
input,
label {
  margin-bottom: 0.5rem;
  display: block;
  width: 100%;
}

* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

body {
  margin: 0;
}

#app {
  margin: 3rem auto;
  max-width: 40rem;
  padding: 1rem;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
}

label {
  font-weight: bold;
}

ul {
  list-style: none;
  margin: 1rem 0;
  padding: 0;
}

li {
  margin: 1rem 0;
  padding: 1rem;
  border: 1px solid #ccc;
}

/*# sourceMappingURL=styles.css.map */
</style>
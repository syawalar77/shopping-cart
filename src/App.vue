<template>
  <div id="app">
    <Header/>
    <div>
      <div class="container">
        <div class="row">
          <div class="col-8">
            <ProductList/>
          </div>
          <div class="col-4">
            <Cart/>
          </div>

        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from './components/mollecules/Header'
import ProductList from './components/ProductList.vue'
import Cart from './components/Cart'
export default {
  components: {
    Header,
    ProductList,
    Cart,
  },

  name: 'App',
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>

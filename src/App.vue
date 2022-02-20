<template>
  <div id="app">
    <HeaderApp />
    <router-view v-bind:catalog="products"
                 v-bind:cart="cart"
                 v-on:add-product="addToCart"
                 v-on:remove-product="removeFromCart" />
    <div class="clear_booth"></div>
    <Footer />
  </div>
</template>

<script>
import HeaderApp from './components/HeaderApp.vue'
import Products from './products.json';
import Footer from './components/FooterApp'

export default {
  name: 'app',
  data() {
    return {
      products: [],
      cart: [],
    }
  },
  mounted() {
    this.products = Products
    this.cart = JSON.parse(window.localStorage.getItem('cart-list')) || []
  },
  components: {
    HeaderApp,
    Footer
  },
  methods: {
    removeFromCart(id) {
      const indx = this.cart.findIndex((item) => item.id === id)
      this.cart.splice(indx, 1)
      window.localStorage.setItem('cart-list', JSON.stringify(this.cart))
    },
    addToCart(id) {
      const product = this.products.find((itemId) => itemId.id === id)
      this.cart.push(product)
      window.localStorage.setItem('cart-list', JSON.stringify(this.cart))
    }
  }
}

</script>

<style lang="scss">

* {
  margin: 0 auto;
  padding: 0;
}
html {
  background: #E5E5E5;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  overflow: hidden;
  position: relative;
  background: rgba(255, 254, 251, 0.8);
}
.clear_booth {
  float: left;
  width: 100%;
  min-height: 180px;
}

</style>

<template>
  <div class="page">
    <h2>Корзина</h2>
    <div class="product-list">
      <ProductCard v-for="item of cart" v-bind:key="item.id" v-bind:data="item" >
        <button class="btn btn-cart" v-on:click="remove(item.id)">Удалить</button>
      </ProductCard>
    </div>
  </div>
</template>

<script>
import ProductCard from '../src/components/ProductCard'

export default {
  name: 'Cart',
  components: { ProductCard },
  props: [
     'cart',
    'catalog'
  ],
  methods: {
    remove(id) {
      this.$emit('remove-product', id)
    }
  }
}
</script>

<style>
.btn-cart {
  width: 161px;
}
</style>
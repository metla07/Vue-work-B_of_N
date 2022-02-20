<template>
  <div class="card">
    <div class="product-container">
      <img require :src="data.url" alt="jpeg" class="div-product-img" width="332" height="200">
      <h3 class="h3-product">{{ data.name }}</h3>
      <p class="p-body-product">{{ data.description }}</p>
      <span class="span-group-price">{{ data.price }} $</span>
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductCard',
  props: [
    'data'
  ]
}
</script>

<style>
.card {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  padding: 20px;

}

.product-container {
  transition: 0.3s;
  list-style: none;
  position: relative;
  margin: 1px 17px 14px 0;
  padding: 15px;
  width: 332px;
  height: 423px;
  cursor: url("../assets/Vector.png"), pointer;
  background: #FFFEFB;
  box-shadow: 0 10px 14px rgba(0, 0, 0, 0.8), 0 1px 5px rgba(0, 0, 0, 0.5);
  border-radius: 4px;
}

.product-container:hover {
  transform: scale(1.1);
  transition: 0.3s;
  box-shadow: 0 20px 24px rgba(0, 0, 0, 0.8), 0 10px 15px rgba(0, 0, 0, 0.5);
}

.product-container:hover .span-group-price {
  font-size: 26px;
}

.div-product-img {
  width: 337px;
  position: absolute;
  left: 12px;
  height: 200px;
  border-radius: 4px 4px 0 0;
  box-shadow: 1px 3px 10px 3px grey;
}

.h3-product {
  position: absolute;
  width: 211px;
  height: 25px;
  left: 70px;
  bottom: 182px;
  font-family: 'Source Sans Pro', sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 20px;
  line-height: 25px;
  color: #3F3F3F;
  letter-spacing: 0.01em;
}

.p-body-product {
  position: absolute;
  width: 300px;
  height: 80px;
  left: 30px;
  bottom: 87px;
  text-align: left;
  font-family: 'Source Sans Pro', sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 18px;
  line-height: 20px;
  color: #3F3F3F;
}

.span-group-price {
  position: absolute;
  width: 100px;
  height: 30px;
  left: 30px;
  bottom: 23px;
  letter-spacing: 0.02em;
  text-align: center;
  font-family: 'Source Sans Pro', sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 30px;
  color: green;
}

</style>
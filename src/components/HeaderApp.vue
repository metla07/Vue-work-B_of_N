<template>
  <header id="header-app">
    <h1>BEAUTY of NATURE</h1>
    <nav class="header-nav">
      <router-link class="router-link" to="/">Главная</router-link>
      <router-link class="router-link" to="/cart">Корзина</router-link>
    </nav>
  </header>
</template>
<script>
export default {
  name: 'header-app',
  data() {
    return {}
  },
  methods: {}
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Source+Sans+Pro&display=swap');

#header-app {
  display: flex;
  justify-content: right;
  align-items: center;
  width: 100%;
  min-height: 60px;
  background: grey;
  position: relative;
}

h1 {
  position: absolute;
  width: 350px;
  height: 35px;
  left: 10px;
  top: 13px;
  font-family: 'Source Sans Pro', sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 37px;
  line-height: 35px;
  color: #3F3F3F;
  letter-spacing: 0.07em;
  text-shadow: 1px 1px 2px greenyellow;
  transition: 1s;
}

h1:hover {
  color: green;
  transition: 0.5s;
}

.header-nav {
  display: flex;
  margin: 0 100px 0 0;
  width: 160px;
  align-content: flex-end;
}

.router-link {
  text-decoration: none;
  margin-left: 10px;
  color: white;
  font-family: 'Source Sans Pro', sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 16px;
  background-color: #B4B4B4;
  padding: 5px;
  border-radius: 4px 4px;
  box-shadow: 0 2px 1px 1px white;
}

.router-link:hover {
  background-color: #F1F4F3;
  box-shadow: 0 2px 1px 1px darkgray;
  color: #3F3F3F;
  transition: 0.5s;

}

.router-link:active {
  box-shadow: 0 1px 0 1px gray;
  background-color: #E5E5E5;
  transition: 0.2s;
}

@media (max-width: 610px) {
  #header-app {
    height: 150px;
    display: flex;
    align-content: flex-end;
  }

  h1 {
    width: 100%;
  }

  .header-nav {
    width: 100%;
    justify-content: center;
    margin: 0;
  }

  .router-link {
    align-self: center;
    margin-top: 30px;
    margin-right: 20px;
  }
}

@media (max-width: 360px) {
  #header-app {
    min-width: 360px;
    height: 150px;
    display: flex;
    align-content: flex-end;
  }

  .router-link {
    margin-top: 30px;
    margin-right: 20px;
  }
}
</style>



<template>
  <div class="sidebar_wrapper">
  <h1 class="sidebar_h1">Лента</h1>
  <div class="sidebar_wrapper_hidden">
   <div class="sidebar">
      <div class="container_img_sidebar img_1"></div>
     <span>

        <i class="icon-heart-empty"></i>
        <i class="icon-thumbs-up"></i>
     </span>
      <p class="sidebar_p">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Asperiores aspernatur deserunt dolorem doloremque, dolores ea earum enim est eveniet fuga in magnam neque nulla officiis possimus qui quibusdam quisquam ut!</p>
      <div class="container_img_sidebar img_2"></div>
     <span>
        <i class="icon-heart-empty"></i>
        <i class="icon-thumbs-up"></i>
     </span>
      <p class="sidebar_p">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci consequuntur cumque expedita inventore libero nobis nostrum rem!</p>
      <div class="container_img_sidebar img_3"></div>
     <span>
        <i class="icon-heart-empty"></i>
        <i class="icon-thumbs-up"></i>
     </span>
      <p class="sidebar_p">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor earum officiis voluptatum?</p>
      <div class="container_img_sidebar img_4"></div>
     <span>
        <i class="icon-heart-empty"></i>
        <i class="icon-thumbs-up"></i>
     </span>
      <p class="sidebar_p">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fugit, laudantium sequi. A animi corporis dolore hic modi officiis reprehenderit temporibus voluptatum! Doloremque dolorum fugiat magni maxime necessitatibus, nemo nihil odio perspiciatis repudiandae similique! Exercitationem, vitae?</p>
   </div>
  </div>
  </div>
</template>
<script>
export default {
  name: 'Sidebar',
  // props: [
  //   'data'
  // ],
  // computed: {
  //   quantity: {
  //     get() {
  //       console.log(this.data)
  //       return this.data
  //     }
  //   },
  //   methods: {
  //     console() {
  //       console.log(this.data)
  //     }
  //   }
  // }
}
</script>
<style lang="scss">
@media (max-width: 980px) {
  .sidebar_wrapper {
    float: right;
    visibility: hidden;
    height: 350px;
  }
}
.sidebar_wrapper {
  position: relative;
  border: 4px solid red;
  top: 80px;
  right: 10px;
  float: right;

}
.sidebar_wrapper_hidden {
  overflow: hidden auto;
  height: 480px;
  width: 400px;
  margin-top: 60px;

}
.sidebar_h1 {
  position: absolute;
  top: 0;
  left: 0;
  height: 50px;
  margin: 0;
  padding: 5px;
  width: 387px;
  border: 1px solid black;
  background-color: lightblue;
}
.sidebar {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 400px;
  min-height: 480px;
  border: 1px solid black;
  box-shadow: 0 2px 8px 0 black;
  background-color: ghostwhite;

  .sidebar_p {
    min-height: 70px;
    width: 400px;
    border: 1px solid black;
  }

  .container_img_sidebar {
    width: 100%;
    height: 200px;
    border: 1px solid black;
    margin: 20px 4px 4px 4px;

  }

  .img_1 {
    background-image: url("../../public/img_1.jpg");
    background-repeat: no-repeat;
    background-size: contain;
    background-position: center;
  }

  .img_2 {
    background-image: url("../../public/img_2.jpg");
    background-repeat: no-repeat;
    background-size: contain;
    background-position: center;
  }

  .img_3 {
    background-image: url("../../public/img_3.jpg");
    background-repeat: no-repeat;
    background-size: contain;
    background-position: center;
  }

  .img_4 {
    background-image: url("../../public/img_4.jpg");
    background-repeat: no-repeat;
    background-size: contain;
    background-position: center;
  }

  .container_i {
    border: 1px solid black;
    width: 100%;
    align-self: end;
  }
  span {
    display: flex;
    justify-content: space-around;
    width: 100%;
    height: 50px;
    padding: 5px;
    align-items: center;
  }

  i {
    color: blue;
    width: 50px;
    height: 50px;
    line-height: 50px;
    font-size: 30px;
    background-color: lightblue;
    border: 2px solid blue;
  }
  i:hover {
    border: 2px solid red;
    color: red;
  }

}
</style>
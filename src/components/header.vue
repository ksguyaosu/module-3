<template>
  <div class="header">
    <img src="../assets/logo.png" />
    <nav class="navMenu">
      <a href="#">Главная</a>
      <a href="#">Каталог</a>
      <a href="#">Блог</a>
      <a href="#">Решения</a>
      <a href="#">Контакты</a>
      <div class="dot"></div>
    </nav>
    <div class="icons">
      <link
        rel="stylesheet"
        href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0"
      />
      <span class="material-symbols-outlined search_icon"> search </span>
      <link
        rel="stylesheet"
        href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200"
      />
      <span class="material-symbols-outlined shopping_cart_icon">
        shopping_cart
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: `headers`,
};
</script>

<style scoped>
img {
  margin-left: 150px;
  margin-top: 32px;
  width: 126px;
  height: 32px;
}
.header {
  /*margin: 0px;*/
  background: #d3cbc5;
  height: 79px;
  display: flex;
  justify-content: space-between;
}
.navMenu {
  margin-top: 5px;
}
.navMenu a {
  color: black;
  text-decoration: none;
  font-size: 1.1em;
  text-transform: uppercase;
  font-weight: 500;
  display: inline-block;
  width: 80px;
  -webkit-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  margin: 0px 10px 0px 10px;
}
.material-symbols-outlined {
  font-variation-settings: "FILL" 0, "wght" 400, "GRAD" 0, "opsz" 48;
}
.search_icon {
  margin-right: 27px;
  cursor: pointer;
}
.shopping_cart_icon {
  cursor: pointer;
}
.icons {
  margin-right: 154px;
  margin-top: 32px;
}
</style>

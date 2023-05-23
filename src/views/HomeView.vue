<template>
  <headers />
  <div class="home">
    <div class="catalog">
      <hr class="line" align="center" width="55" size="2" color="#9a6437" />
      <br />
      <p>КАТАЛОГ</p>
    </div>
    <div class="bestsellers">
      <h1>Лучшие новинки</h1>
      <div class="selectors">
        <button class="select_btn">Мебель</button>
        <button class="select_btn">Свет</button>
        <button class="select_btn">Декор</button>
      </div>
    </div>
    <div class="product">
      <product_page
        v-for="product in products"
        :key="product.name"
        :product_data="product"
      />
    </div>
    <!--    <img alt="Vue logo" src="../assets/logo.png" />-->
    <!--    <HelloWorld msg="Welcome to Your Vue.js App" />-->
  </div>
  <footers />
</template>

<script>
import headers from "@/components/header";
import product_page from "@/components/product_page";
import footers from "@/components/footer";
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "HomeView",
  components: {
    product_page,
    headers,
    footers,
    // HelloWorld,
  },
  data() {
    return {
      products: [
        {
          name: "Кресло",
          price: 4000,
          discountPrice: 3500,
          category: "мебель",
          parameters: "700x1000x600",
          weight: 3.5,
          image: "1.png",
        },
        {
          name: "Кресло",
          price: 3400,
          discountPrice: 3100,
          category: "мебель",
          parameters: "800x900x600",
          weight: 3.6,
          image: "2.png",
        },
        {
          name: "Ваза для цветов",
          price: 1100,
          category: "декор",
          parameters: "150x250x150",
          weight: 0.6,
          image: "3.png",
        },
        {
          name: "Стул",
          price: 2300,
          category: "мебель",
          parameters: "600x1200x600",
          weight: 1.5,
          image: "4.png",
        },
        {
          name: "Лампа",
          price: 4800,
          category: "свет",
          parameters: "200x600x300",
          weight: 1.0,
          image: "5.png",
        },
        {
          name: "Ваза для цветов",
          price: 2300,
          discountPrice: 1900,
          category: "декор",
          parameters: "200x300x300",
          weight: 0.3,
          image: "6.png",
        },
        {
          name: "Серый стул",
          price: 4100,
          discountPrice: 2500,
          category: "мебель",
          parameters: "600x1200x600",
          weight: 2.5,
          image: "7.png",
        },
        {
          name: "Черный стул",
          price: 3300,
          category: "мебель",
          parameters: "700x1000x700",
          weight: 1.9,
          image: "8.png",
        },
      ],
    };
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
headers {
  height: 79px;
}
.product {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
}
.home {
  margin-left: 150px;
  margin-right: 149px;
}
.catalog {
  display: flex;
  margin-top: 46px;
  margin-bottom: 21px;
}
.catalog p {
  font-size: 16px;
  color: #9a6437;
}
.line {
  margin-right: 10px;
  margin-top: 8px;
}
.bestsellers {
  display: flex;
  justify-content: space-between;
}
.select_btn {
  border: none;
  background: white;
  cursor: pointer;
  margin: 0 10px 0 10px;
  padding: 5px;
}
.select_btn:active {
  background: #000;
  color: white;
}
.select_btn:visited {
  background: #000;
  color: white;
}
.select_btn:focus {
  background: #000;
  color: white;
}
</style>

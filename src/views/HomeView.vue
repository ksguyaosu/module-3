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
        <button class="select_btn" v-on:click="filterByFurniture">
          Мебель
        </button>
        <button class="select_btn" v-on:click="filterByLight">Свет</button>
        <button class="select_btn" v-on:click="filterByDecor">Декор</button>
        <button class="select_btn" v-on:click="filterByAll">
          Все категории
        </button>
      </div>
    </div>
    <div class="product">
      <product_page
        v-for="product in filteredProducts"
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
        {
          name: "Стул",
          price: 3900,
          discountPrice: 3500,
          category: "мебель",
          parameters: "600x1200x600",
          weight: 1.5,
          image: "9.png",
        },
        {
          name: "Стул",
          price: 4500,
          category: "мебель",
          parameters: "600x1200x600",
          weight: 2.5,
          image: "10.png",
        },
        {
          name: "Диван серый",
          price: 20000,
          category: "мебель",
          parameters: "1200x1000x800",
          weight: 8.5,
          image: "11.png",
        },
        {
          name: "Диван желтый",
          price: 34000,
          discountPrice: 30500,
          category: "мебель",
          parameters: "2000x1000x900",
          weight: 10.5,
          image: "12.png",
        },
        {
          name: "Кресло синее",
          price: 7000,
          category: "мебель",
          parameters: "800x1000x8600",
          weight: 3.5,
          image: "13.png",
        },
        {
          name: "Кресло зеленое",
          price: 8000,
          category: "мебель",
          parameters: "800x1000x800",
          weight: 3.0,
          image: "14.png",
        },
      ],
      sortedProducts: [],
    };
  },
  computed: {
    filteredProducts() {
      if (this.sortedProducts.length) {
        return this.sortedProducts;
      } else {
        return this.products;
      }
    },
  },
  methods: {
    filterByFurniture() {
      this.sortedProducts = this.products.filter(function (e) {
        return e.category === "мебель";
      });
    },
    filterByLight() {
      this.sortedProducts = this.products.filter(function (e) {
        return e.category === "свет";
      });
    },
    filterByDecor() {
      this.sortedProducts = this.products.filter(function (e) {
        return e.category === "декор";
      });
    },
    filterByAll() {
      this.sortedProducts = this.products;
    },
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

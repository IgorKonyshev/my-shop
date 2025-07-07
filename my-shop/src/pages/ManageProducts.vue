<template>
  <div>
    <h1>Пошук товарів</h1>
    <input
      type="text"
      v-model="searchQuery"
      placeholder="Введіть назву товару"
    />
    <ProductList :products="filteredProducts" />
  </div>
</template>

<script>
import ProductList from "@/components/ProductList.vue";

export default {
  components: {
    ProductList,
  },
  data() {
    return {
      searchQuery: "",
      products: [
        {
          id: 1,
          name: "Смартфон Samsung Galaxy S23",
          description: "Потужний флагманський смартфон",
          price: 35000,
          image: "https://img.freepik.com/free-photo/white-cell-phone-box-background_58702-4721.jpg",
        },
        {
          id: 2,
          name: "Ноутбук Apple MacBook Air M2",
          description: "Легкий, потужний та стильний ноутбук",
          price: 58000,
          image: "https://img.freepik.com/free-photo/workplace-with-laptop-stand-near-eyeglasses_23-2148040478.jpg",
        },
        {
          id: 3,
          name: "Навушники Sony WH-1000XM4",
          description: "Бездротові з шумозаглушенням",
          price: 7800,
          image: "https://img.freepik.com/free-photo/closeup-shot-white-wireless-headphones-with-their-case-white-background_181624-31412.jpg",
        },
        {
          id: 4,
          name: "Механічна клавіатура HyperX",
          description: "Для геймерів та програмістів",
          price: 4500,
          image: "https://img.freepik.com/free-photo/top-view-keyboard-mouse-arrangement_23-2149386333.jpg",
        },
        {
          id: 5,
          name: "Смарт-годинник Apple Watch Series 9",
          description: "Здоров’я, спорт, повідомлення – все на зап’ясті",
          price: 17000,
          image: "https://img.freepik.com/free-photo/modern-sport-adult-hand-lifestyle_1127-2745.jpg",
        },
      ],
    };
  },
  computed: {
    filteredProducts() {
      const query = this.searchQuery.toLowerCase();
      return this.products.filter((product) =>
        product.name.toLowerCase().includes(query)
      );
    },
  },
};
</script>
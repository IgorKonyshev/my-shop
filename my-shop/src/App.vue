<template>
  <div id="app" class="app-container">
    <FooterComponent />
  </div>
  <div id="app">
    <ProductList />
  </div>
</template>

<script>
import FooterComponent from "./components/FooterComponent.vue";

export default {
  name: "App",
  components: {
    FooterComponent,
  },
};
</script>

<script>
import ProductList from "@/components/ProductList.vue";
export default {
  name: "App",
  components: {
    ProductList,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<style>
html,
body,
#app {
  height: 100%;
  margin: 0;
}
.app-container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
</style>

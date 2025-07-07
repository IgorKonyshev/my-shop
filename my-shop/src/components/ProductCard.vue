<template>
  <div class="card">
    <img :src="image" alt="Зображення товару" />
    <h3>{{ name }}</h3>
    <p>{{ description }}</p>
    <strong>{{ price }} грн</strong>
     <button @click="addToCart">Додати до кошика</button>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    description: String,
    price: Number,
    image: String,
  },
};
</script>

<style scoped>
.card {
  width: 220px;
  padding: 1rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  text-align: center;
  background: white;
}
.card img {
  width: 100%;
  border-radius: 8px;
  margin-bottom: 0.5rem;
}
</style>

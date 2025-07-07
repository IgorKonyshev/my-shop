<template>
  <div class="cart">
    <h2>Кошик покупок</h2>

    <p v-if="!cartItems.length">Кошик порожній</p>

    <ul v-else>
      <li v-for="(item, index) in cartItems" :key="index">
        <img :src="item.image" :alt="item.name" width="50" />
        {{ item.name }} – {{ item.price }} грн
        <button @click="removeItem(index)">Видалити</button>
      </li>
    </ul>

    <p v-if="cartItems.length > 0">
      <strong>Загальна сума: {{ totalPrice }} грн</strong>
    </p>
  </div>
</template>

<script>    
export default {
  props: {
    cartItems: Array,
  },
  emits: ["remove"],
  computed: {
    totalPrice() {
      return this.cartItems.reduce((sum, item) => sum + item.price, 0);
    },
  },
  methods: {
    removeItem(index) {
      this.$emit("remove", index);
    },
  },
};
</script>

<style scoped>
.cart {
  border: 1px solid #ccc;
  padding: 20px;
  margin-top: 20px;
}
</style>
<template>
  <div class="admin-dashboard">
    <nav>
      <ul>
        <li><router-link to="/admin/products">Продукти</router-link></li>
        <li><router-link to="/admin/reviews">Відгуки</router-link></li>
        <li><router-link to="/admin/orders">Замовлення</router-link></li>
      </ul>
    </nav>

    <main>
      <router-view />
    </main>
  </div>
</template>

<script>
export default {
  name: "AdminDashboard",
};
</script>

<style scoped>
nav ul {
  list-style: none;
  padding: 0;
  display: flex;
  gap: 1rem;
}
</style>
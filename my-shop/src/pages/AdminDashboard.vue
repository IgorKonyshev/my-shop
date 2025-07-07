<template>
  <div>
    <header class="header">
      <div class="logo">Сайт Ігорька</div>
      <nav class="nav">
        <router-link to="/admin/products" active-class="active-link">Головна</router-link>
        <router-link to="/admin/reviews" active-class="active-link">Відгуки</router-link>
      </nav>
    </header>

    <main class="main">
      <router-view />
    </main>
  </div>
</template>

<script>
export default {
  name: 'AdminDashboard'
}
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  background-color: #2c3e50;
  color: white;
  position: sticky;
  top: 0;
  z-index: 10;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
}

.nav {
  display: flex;
  gap: 1.5rem;
}

.nav a {
  color: white;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s ease;
}

.nav a:hover {
  color: #1abc9c;
}

.active-link {
  border-bottom: 2px solid #1abc9c;
  padding-bottom: 2px;
}

.main {
  padding: 2rem;
}
</style>
<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="contact-info">
        <h3>Контактна інформація</h3>
        <p>Email: info@example.com</p>
        <p>Телефон: +38 (097) 123-45-67</p>
      </div>
      <div class="footer-links">
        <h3>Корисні посилання</h3>
        <ul>
          <li><a href="/about">Про нас</a></li>
          <li><a href="/delivery">Доставка</a></li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
};
</script>

<style scoped>
.footer {
  background-color: #f8f8f8;
  color: #333;
  padding: 2rem 1rem;
  border-top: 1px solid #ddd;
  margin-top: auto;
}
.footer-content {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  max-width: 1200px;
  margin: 0 auto;
}
.contact-info,
.footer-links {
  flex: 1 1 300px;
  margin-bottom: 1rem;
}
.footer-links ul {
  list-style: none;
  padding: 0;
}
.footer-links a {
  text-decoration: none;
  color: #007bff;
}
.footer-links a:hover {
  text-decoration: underline;
}
</style>

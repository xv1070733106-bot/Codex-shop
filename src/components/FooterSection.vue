<template>
  <footer class="footer">
    <div class="container">
      <div class="brand">琥珀</div>
      <div class="footer-social">
        <a href="#">微信</a>
        <a href="#">小红书</a>
        <a href="#">Instagram</a>
      </div>
      <p>&copy; 2026 琥珀 · 现代亚洲料理 · All Rights Reserved</p>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background: #121212;
  color: rgba(255, 255, 255, 0.5);
  padding: 48px 0 32px;
  text-align: center;
  font-size: 13px;
  letter-spacing: 1px;
  font-weight: 300;
}
.footer .brand {
  font-family: 'Noto Serif SC', serif;
  font-size: 18px;
  color: rgba(255, 255, 255, 0.4);
  letter-spacing: 6px;
  margin-bottom: 12px;
}
.footer-social {
  display: flex;
  justify-content: center;
  gap: 24px;
  margin-bottom: 16px;
}
.footer-social a {
  color: rgba(255, 255, 255, 0.35);
  font-size: 13px;
  transition: color 0.3s;
}
.footer-social a:hover {
  color: #c8a87c;
}
</style>

<template>
  <section class="menu" id="menu">
    <div class="container">
      <div class="section-header">
        <div class="section-tag">Signature</div>
        <h2 class="section-title">招牌菜品</h2>
        <p class="section-desc">精选当季食材，每道菜都承载着我们对味道的理解与坚持</p>
      </div>
      <div class="dishes">
        <div class="dish-card">
          <div
            class="dish-img"
            style="background-image: url('https://images.unsplash.com/photo-1546069901-ba9599a7e63c?w=600&q=80')"
          ></div>
          <div class="dish-body">
            <h4>炭烤和牛</h4>
            <div class="price">¥ 388</div>
            <p>澳洲 M7 和牛，备长炭锁住汁水，山椒酱解腻提鲜，搭配当季时蔬</p>
          </div>
        </div>
        <div class="dish-card">
          <div
            class="dish-img"
            style="background-image: url('https://images.unsplash.com/photo-1565299624946-b28f40a0ae38?w=600&q=80')"
          ></div>
          <div class="dish-body">
            <h4>松露烩饭</h4>
            <div class="price">¥ 268</div>
            <p>意大利 Carnaroli 米慢煮至粒粒柔糯，黑松露刨片，帕玛森泡沫轻覆如云</p>
          </div>
        </div>
        <div class="dish-card">
          <div
            class="dish-img"
            style="background-image: url('https://images.unsplash.com/photo-1551218808-94e220e084d2?w=600&q=80')"
          ></div>
          <div class="dish-body">
            <h4>柚子渍带子</h4>
            <div class="price">¥ 188</div>
            <p>北海道鲜带子薄切冰镇，柚子酱清酸开场，鱼子酱咸鲜收尾</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.menu {
  background: #faf9f7;
}
.dishes {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 28px;
}
.dish-card {
  background: #fff;
  overflow: hidden;
  transition: transform 0.4s, box-shadow 0.4s;
  border: 1px solid #f0ece6;
}
.dish-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 12px 36px rgba(0, 0, 0, 0.06);
}
.dish-img {
  height: 240px;
  background-size: cover;
  background-position: center;
}
.dish-body {
  padding: 28px 24px 32px;
}
.dish-body h4 {
  font-family: 'Noto Serif SC', serif;
  font-size: 18px;
  font-weight: 600;
  margin-bottom: 6px;
  letter-spacing: 2px;
}
.dish-body .price {
  font-size: 14px;
  color: #c8a87c;
  font-weight: 500;
  margin-bottom: 10px;
  letter-spacing: 1px;
}
.dish-body p {
  font-size: 14px;
  color: #777;
  line-height: 1.7;
  font-weight: 300;
}
</style>

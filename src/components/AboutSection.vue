<template>
  <section class="about" id="about">
    <div class="container">
      <div class="section-header">
        <div class="section-tag">Our Story</div>
        <h2 class="section-title">关于水晶</h2>
      </div>
      <div class="about-grid">
        <div class="about-image"></div>
        <div class="about-text">
          <h3>好好吃饭</h3>
          <p>水晶 2018 年开张。我们挑选好的食材，用简单的方法烹饪，让食物自己说话。没什么复杂的理念，就是想认真做好每道菜，让来的客人吃得舒服。</p>
          <p>主厨林逸晨在东京、曼谷的厨房里待过很多年。水晶没有太多噱头——只想用诚实的味道，招待每一位推门进来的你。</p>
          <div class="about-signature">
            <strong>林逸晨</strong>
            <span>创始人 &amp; 行政主厨</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about {
  background: #fff;
}
.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
}
.about-image {
  height: 480px;
  overflow: hidden;
  background: url('https://images.unsplash.com/photo-1552566626-52f8b828add9?w=800&q=80') center / cover no-repeat;
}
.about-text h3 {
  font-family: 'Noto Serif SC', serif;
  font-size: 26px;
  font-weight: 600;
  margin-bottom: 20px;
  letter-spacing: 3px;
}
.about-text p {
  font-size: 15px;
  line-height: 1.9;
  color: #555;
  margin-bottom: 16px;
  font-weight: 300;
}
.about-signature {
  margin-top: 32px;
  padding-top: 24px;
  border-top: 1px solid #e8e4df;
}
.about-signature strong {
  font-family: 'Noto Serif SC', serif;
  font-size: 18px;
  letter-spacing: 2px;
  display: block;
  color: #1a1a1a;
}
.about-signature span {
  font-size: 13px;
  color: #999;
  letter-spacing: 2px;
}
</style>

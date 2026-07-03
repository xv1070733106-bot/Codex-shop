<template>
  <section class="contact" id="contact">
    <div class="container">
      <div class="section-header">
        <div class="section-tag">Contact</div>
        <h2 class="section-title">联系我们</h2>
      </div>
      <div class="contact-grid">
        <div>
          <div class="contact-item"><h4>地址</h4><p>上海市黄浦区外滩 18 号 6 楼</p></div>
          <div class="contact-item"><h4>电话</h4><p><a href="tel:02163887799">021-6388 7799</a></p></div>
          <div class="contact-item"><h4>邮箱</h4><p><a href="mailto:reserve@hupo.sh">reserve@hupo.sh</a></p></div>
        </div>
        <div>
          <div class="contact-item"><h4>交通</h4><p>地铁 2/10 号线南京东路站，步行约 8 分钟。<br />自驾可停外滩源停车场。</p></div>
          <div class="contact-item"><h4>包厢</h4><p>提供 2 间私人包厢（6 位 / 12 位），<br />需提前三天预约并确认菜单。</p></div>
        </div>
      </div>
      <div class="map-placeholder">地图加载中</div>
    </div>
  </section>
</template>

<style scoped>
.contact {
  background: #fff;
}
.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 48px 60px;
}
.contact-item {
  margin-bottom: 32px;
}
.contact-item h4 {
  font-family: 'Noto Serif SC', serif;
  font-size: 14px;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 2px;
  margin-bottom: 8px;
  color: #1a1a1a;
}
.contact-item p,
.contact-item a {
  font-size: 14px;
  color: #666;
  line-height: 1.8;
  font-weight: 300;
}
.contact-item a:hover {
  color: #c8a87c;
}
.map-placeholder {
  height: 300px;
  background: #f5f2ed;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 13px;
  color: #aaa;
  letter-spacing: 2px;
  border: 1px solid #ece8e2;
  margin-top: 48px;
}
</style>

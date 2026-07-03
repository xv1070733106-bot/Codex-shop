<template>
  <section class="reserve" id="reserve">
    <div class="container">
      <div class="section-header">
        <div class="section-tag">Reservation</div>
        <h2 class="section-title">预约订座</h2>
        <p class="section-desc">午市与晚市开放预约，建议提前两天预订</p>
      </div>
      <div class="reserve-card">
        <div class="info-row"><span class="label">午市</span><span class="value">11:30 – 14:00（最后点单 13:30）</span></div>
        <div class="info-row"><span class="label">晚市</span><span class="value">17:30 – 22:00（最后点单 21:00）</span></div>
        <div class="info-row"><span class="label">休息日</span><span class="value">每周一</span></div>
        <div class="info-row"><span class="label">电话</span><span class="value">021-6388 7799</span></div>
        <button class="reserve-btn">在线预约</button>
      </div>
    </div>
  </section>
</template>

<style scoped>
.reserve {
  background: #1a1a1a;
  color: #fff;
  text-align: center;
}
.reserve .section-title {
  color: #fff;
}
.reserve .section-desc {
  color: rgba(255, 255, 255, 0.6);
}
.reserve-card {
  max-width: 580px;
  margin: 0 auto;
  padding: 48px 40px;
  border: 1px solid rgba(200, 168, 124, 0.25);
}
.reserve-card .info-row {
  display: flex;
  justify-content: space-between;
  padding: 14px 0;
  border-bottom: 1px solid rgba(255, 255, 255, 0.06);
  font-size: 14px;
  letter-spacing: 1px;
}
.reserve-card .info-row:last-child {
  border-bottom: none;
}
.reserve-card .label {
  color: rgba(255, 255, 255, 0.45);
  text-transform: uppercase;
  font-size: 12px;
}
.reserve-card .value {
  color: rgba(255, 255, 255, 0.85);
}
.reserve-btn {
  margin-top: 36px;
  display: inline-block;
  padding: 14px 48px;
  background: #c8a87c;
  color: #1a1a1a;
  font-size: 13px;
  font-weight: 600;
  letter-spacing: 3px;
  border: none;
  cursor: pointer;
  transition: opacity 0.3s;
}
.reserve-btn:hover {
  opacity: 0.85;
}
</style>

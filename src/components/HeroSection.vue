<script setup lang="ts">
const emit = defineEmits<{ navigate: [id: string] }>()
</script>

<template>
  <section class="hero" id="hero">
    <div class="hero-bg"></div>
    <div class="hero-content">
      <div class="hero-suptitle">Est. 2018 · Shanghai</div>
      <h1 class="hero-title">琥珀</h1>
      <p class="hero-sub">现代亚洲料理 · 时令食材 · 匠心呈现</p>
      <a href="#reserve" class="hero-btn" @click.prevent="emit('navigate', '#reserve')">预约订座</a>
    </div>
    <div class="hero-scroll">
      向下探索
      <div class="line"></div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  position: relative;
  height: 100vh;
  min-height: 600px;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}
.hero-bg {
  position: absolute;
  inset: 0;
  background: url('https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?w=1920&q=80') center / cover no-repeat;
  transform: scale(1.03);
  transition: transform 8s ease;
}
.hero-bg::after {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, rgba(0, 0, 0, 0.72) 0%, rgba(0, 0, 0, 0.45) 50%, rgba(0, 0, 0, 0.72) 100%);
}
.hero:hover .hero-bg {
  transform: scale(1);
}
.hero-content {
  position: relative;
  z-index: 2;
  text-align: center;
  color: #fff;
  padding: 0 24px;
  max-width: 780px;
}
.hero-suptitle {
  font-size: 13px;
  letter-spacing: 6px;
  text-transform: uppercase;
  color: #c8a87c;
  margin-bottom: 20px;
  font-weight: 500;
}
.hero-title {
  font-family: 'Noto Serif SC', serif;
  font-size: clamp(48px, 8vw, 88px);
  font-weight: 700;
  letter-spacing: 12px;
  margin-bottom: 16px;
  line-height: 1.2;
}
.hero-sub {
  font-size: 15px;
  font-weight: 300;
  color: rgba(255, 255, 255, 0.7);
  letter-spacing: 3px;
  margin-bottom: 40px;
}
.hero-btn {
  display: inline-block;
  padding: 14px 44px;
  border: 1.5px solid #c8a87c;
  color: #c8a87c;
  font-size: 13px;
  font-weight: 500;
  letter-spacing: 3px;
  transition: all 0.35s;
  cursor: pointer;
  background: transparent;
}
.hero-btn:hover {
  background: #c8a87c;
  color: #1a1a1a;
}
.hero-scroll {
  position: absolute;
  bottom: 32px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 2;
  color: rgba(255, 255, 255, 0.5);
  font-size: 11px;
  letter-spacing: 2px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
}
.hero-scroll .line {
  width: 1px;
  height: 36px;
  background: rgba(255, 255, 255, 0.35);
  animation: scrollIn 2s ease-in-out infinite;
}
</style>

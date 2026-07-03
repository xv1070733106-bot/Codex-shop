<script setup lang="ts">
defineProps<{ scrolled: boolean }>()
const emit = defineEmits<{ navigate: [id: string] }>()
</script>

<template>
  <nav class="nav" :class="{ scrolled }">
    <div class="container">
      <a href="#" class="nav-logo">琥珀</a>
      <ul class="nav-links">
        <li><a href="#about" @click.prevent="emit('navigate', '#about')">餐厅</a></li>
        <li><a href="#menu" @click.prevent="emit('navigate', '#menu')">菜品</a></li>
        <li><a href="#reserve" @click.prevent="emit('navigate', '#reserve')">订座</a></li>
        <li><a href="#contact" @click.prevent="emit('navigate', '#contact')">联系</a></li>
      </ul>
    </div>
  </nav>
</template>

<style scoped>
.nav {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  padding: 20px 0;
  background: transparent;
  transition: background 0.35s, padding 0.35s;
  pointer-events: none;
}
.nav.scrolled {
  background: #1a1a1a;
  padding: 12px 0;
  pointer-events: auto;
}
.nav .container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  pointer-events: auto;
}
.nav-logo {
  font-family: 'Noto Serif SC', serif;
  font-size: 22px;
  font-weight: 700;
  color: #fff;
  letter-spacing: 6px;
}
.nav-links {
  display: flex;
  gap: 32px;
}
.nav-links a {
  font-size: 14px;
  font-weight: 500;
  color: rgba(255, 255, 255, 0.78);
  letter-spacing: 1.5px;
  transition: color 0.25s;
  position: relative;
}
.nav-links a::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -3px;
  width: 0;
  height: 1.5px;
  background: #c8a87c;
  transition: width 0.3s;
}
.nav-links a:hover {
  color: #c8a87c;
}
.nav-links a:hover::after {
  width: 100%;
}
</style>

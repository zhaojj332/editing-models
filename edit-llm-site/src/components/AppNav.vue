<template>
  <nav class="app-nav">
    <div class="nav-inner container">
      <div class="nav-items">
        <a href="#" class="nav-item active">首页</a>
        <div class="nav-item nav-dropdown" @mouseenter="showProduct = true" @mouseleave="showProduct = false">
          <span>产品介绍</span>
          <span class="dropdown-arrow">▼</span>
          <div v-show="showProduct" class="dropdown-menu">
            <a href="#" class="dropdown-item">编辑大模型</a>
            <a href="#" class="dropdown-item">智校云雠</a>
          </div>
        </div>
        <div class="nav-item nav-dropdown" @mouseenter="showTips = true" @mouseleave="showTips = false">
          <span>使用技巧</span>
          <span class="dropdown-arrow">▼</span>
          <div v-show="showTips" class="dropdown-menu">
            <a href="#" class="dropdown-item">编辑大模型技巧</a>
            <a href="#" class="dropdown-item">智校云雠技巧</a>
          </div>
        </div>
        <a href="#" class="nav-item">关于我们</a>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'

const showProduct = ref(false)
const showTips = ref(false)
</script>

<style scoped>
.app-nav {
  background: rgba(255, 255, 255, 0.9);
  padding: 0;
  border-radius: var(--radius-full);
  margin: -8px auto 24px;
  max-width: 600px;
  box-shadow: var(--shadow-md);
}

.nav-inner {
  padding: 12px 24px;
}

.nav-items {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
}

.nav-item {
  padding: 12px 24px;
  color: var(--color-text-secondary);
  font-weight: 500;
  border-radius: var(--radius-full);
  transition: all var(--transition-fast);
}

.nav-item:hover,
.nav-item.active {
  color: var(--color-primary);
  background: var(--color-bg-light);
}

.nav-dropdown {
  position: relative;
  cursor: pointer;
}

.dropdown-arrow {
  font-size: 10px;
  margin-left: 4px;
}

.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
  margin-top: 8px;
  background: white;
  border-radius: var(--radius-md);
  padding: 12px 0;
  min-width: 180px;
  box-shadow: var(--shadow-lg);
  z-index: 100;
}

.dropdown-item {
  display: block;
  padding: 12px 24px;
  color: var(--color-text-secondary);
  transition: all var(--transition-fast);
}

.dropdown-item:hover {
  background: var(--color-bg-light);
  color: var(--color-primary);
}
</style>

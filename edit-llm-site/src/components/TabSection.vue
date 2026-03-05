<template>
  <section class="tab-section">
    <div class="container">
      <div class="section-header">
        <h2 class="section-title">产品展示</h2>
        <p class="section-subtitle">标签模块</p>
      </div>
      <div class="tab-wrapper">
        <div class="tab-buttons">
          <button
            v-for="(tab, index) in tabs"
            :key="index"
            class="tab-btn"
            :class="{ active: activeTab === index }"
            @click="activeTab = index"
          >
            {{ tab.name }}
          </button>
        </div>
        <div class="tab-content">
          <div
            v-for="(tab, index) in tabs"
            :key="index"
            class="tab-panel"
            :class="{ active: activeTab === index }"
          >
            <div class="panel-placeholder">
              <span class="panel-icon">{{ tab.icon }}</span>
              <p class="panel-text">{{ tab.name }} 展示区域</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const activeTab = ref(0)

const tabs = [
  { name: '编辑大模型', icon: '🤖' },
  { name: '智校云雠', icon: '☁️' }
]
</script>

<style scoped>
.tab-section {
  padding: 48px 0;
}

.section-header {
  text-align: center;
  margin-bottom: 40px;
}

.section-title {
  font-size: 28px;
  color: var(--color-text-primary);
  margin-bottom: 8px;
}

.section-subtitle {
  font-size: 16px;
  color: var(--color-text-muted);
}

.tab-wrapper {
  background: var(--color-bg-card);
  border-radius: var(--radius-xl);
  overflow: hidden;
  box-shadow: var(--shadow-md);
}

.tab-buttons {
  display: flex;
  padding: 16px 24px;
  gap: 12px;
  background: var(--color-bg-light);
  border-bottom: 1px solid rgba(94, 179, 232, 0.2);
}

.tab-btn {
  padding: 14px 32px;
  font-size: 16px;
  font-weight: 500;
  border: none;
  border-radius: var(--radius-full);
  background: transparent;
  color: var(--color-text-secondary);
  cursor: pointer;
  transition: all var(--transition-fast);
}

.tab-btn:hover {
  color: var(--color-primary);
  background: rgba(94, 179, 232, 0.1);
}

.tab-btn.active {
  background: var(--color-primary);
  color: white;
}

.tab-content {
  padding: 48px;
  min-height: 320px;
}

.tab-panel {
  display: none;
}

.tab-panel.active {
  display: block;
  animation: fadeIn 0.3s ease;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.panel-placeholder {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 220px;
  background: linear-gradient(135deg, var(--color-bg-light) 0%, var(--color-primary-lighter) 20%);
  border-radius: var(--radius-lg);
}

.panel-icon {
  font-size: 64px;
  margin-bottom: 16px;
}

.panel-text {
  font-size: 18px;
  color: var(--color-text-secondary);
}
</style>

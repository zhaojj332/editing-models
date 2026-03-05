<template>
  <header class="app-header">
    <div class="header-inner container">
      <div class="logo-wrap">
        <div class="logo-placeholder">
          <span class="logo-icon">📚</span>
        </div>
        <h1 class="site-title">
          <span class="highlight">高等教育出版社</span>智能审校产品体系
        </h1>
      </div>
    </div>
  </header>
</template>

<script setup>
</script>

<style scoped>
.app-header {
  background: linear-gradient(135deg, rgba(255,255,255,0.95) 0%, rgba(232,244,252,0.98) 100%);
  backdrop-filter: blur(12px);
  padding: 20px 0;
  font-weight: 500;
  border-radius: 0 0 var(--radius-xl) var(--radius-xl);
  box-shadow: var(--shadow-sm);
}

.header-inner {
  display: flex;
  align-items: center;
  gap: 20px;
}

.logo-placeholder {
  width: 56px;
  height: 56px;
  background: linear-gradient(135deg, var(--color-primary) 0%, var(--color-primary-dark) 100%);
  border-radius: var(--radius-full);
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 12px;
}

.logo-icon {
  font-size: 28px;
}

.site-title {
  font-size: 24px;
  color: var(--color-text-primary);
  font-weight: 600;
}

.highlight {
  color: var(--color-primary);
  font-weight: 700;
}
</style>

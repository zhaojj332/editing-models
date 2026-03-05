<template>
  <section class="apply-section">
    <div class="container">
      <div class="apply-card">
        <div class="apply-content">
          <h2 class="apply-title">申请使用</h2>
          <p class="apply-info">咨询热线：010-58581118 &nbsp; 58581116</p>
        </div>
        <a href="https://hep10.feishu.cn/share/base/form/shrcncAyrwONmOMdknaIMDb2sDe" target="_blank" class="btn btn-primary btn-large">
          点击申请
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.apply-section {
  padding: 48px 0;
}

.apply-card {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: linear-gradient(135deg, var(--color-primary) 0%, var(--color-primary-dark) 100%);
  border-radius: var(--radius-xl);
  padding: 48px 64px;
  box-shadow: var(--shadow-lg);
}

.apply-content {
  color: white;
}

.apply-title {
  font-size: 36px;
  font-weight: 700;
  margin-bottom: 12px;
}

.apply-info {
  font-size: 20px;
  opacity: 0.95;
}

.btn-large {
  padding: 18px 48px;
  font-size: 18px;
  background: white;
  color: var(--color-primary);
}

.btn-large:hover {
  background: var(--color-bg-light);
  color: var(--color-primary-dark);
}
</style>

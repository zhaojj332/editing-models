<template>
  <footer class="app-footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-brand">
          <div class="footer-logo">📚</div>
          <h3 class="footer-title">高等教育出版社</h3>
        </div>
        <div class="footer-info">
          <p>联系地址：北京市西城区德外大街4号（100120） &nbsp; 北京市朝阳区惠新东街4号富盛大厦（100029）</p>
          <p>联系电话：010-58581118 &nbsp; 58581116</p>
        </div>
      </div>
      <div class="footer-bottom">
        <p>©2026 - 高等教育出版社智能审校产品体系 版权所有</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
</script>

<style scoped>
.app-footer {
  background: linear-gradient(180deg, var(--color-primary-lighter) 0%, var(--color-primary-light) 100%);
  padding: 48px 0 24px;
  margin-top: 48px;
  border-radius: var(--radius-xl) var(--radius-xl) 0 0;
}

.footer-content {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: 48px;
  padding-bottom: 32px;
  border-bottom: 1px solid rgba(255,255,255,0.5);
}

.footer-brand {
  display: flex;
  align-items: center;
  gap: 16px;
}

.footer-logo {
  font-size: 40px;
}

.footer-title {
  font-size: 24px;
  color: var(--color-primary-darker);
  font-weight: 700;
}

.footer-info {
  flex: 1;
  max-width: 600px;
}

.footer-info p {
  font-size: 14px;
  color: var(--color-text-secondary);
  line-height: 1.8;
}

.footer-bottom {
  padding-top: 24px;
  text-align: center;
}

.footer-bottom p {
  font-size: 14px;
  color: var(--color-text-muted);
}
</style>

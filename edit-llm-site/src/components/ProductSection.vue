<template>
  <section class="product-section">
    <div class="container">
      <div class="product-card" :class="{ reverse: reverse }">
        <div class="product-media">
          <div class="media-placeholder">
            <span class="media-icon">{{ icon }}</span>
          </div>
        </div>
        <div class="product-content">
          <h2 class="product-title">{{ title }}</h2>
          <p class="product-desc">{{ description }}</p>
          <a :href="link" class="btn btn-primary" target="_blank">了解更多</a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
defineProps({
  title: String,
  description: String,
  icon: String,
  link: String,
  reverse: Boolean
})
</script>

<style scoped>
.product-section {
  padding: 48px 0;
}

.product-card {
  display: flex;
  align-items: center;
  gap: 48px;
  background: var(--color-bg-card);
  border-radius: var(--radius-xl);
  padding: 48px;
  box-shadow: var(--shadow-md);
  transition: all var(--transition-normal);
}

.product-card:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-4px);
}

.product-card.reverse {
  flex-direction: row-reverse;
}

.product-media {
  flex: 0 0 320px;
}

.media-placeholder {
  aspect-ratio: 16/10;
  background: linear-gradient(135deg, var(--color-primary-lighter) 0%, var(--color-primary-light) 100%);
  border-radius: var(--radius-lg);
  display: flex;
  align-items: center;
  justify-content: center;
}

.media-icon {
  font-size: 80px;
}

.product-content {
  flex: 1;
}

.product-title {
  font-size: 32px;
  color: var(--color-primary);
  margin-bottom: 20px;
  font-weight: 700;
}

.product-desc {
  font-size: 18px;
  color: var(--color-text-secondary);
  line-height: 1.8;
  margin-bottom: 28px;
}
</style>

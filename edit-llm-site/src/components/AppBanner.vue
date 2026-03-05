<template>
  <section class="app-banner">
    <div class="banner-slider">
      <div 
        v-for="(slide, index) in slides" 
        :key="index"
        class="slide"
        :class="{ active: currentIndex === index }"
      >
        <div class="slide-content" :style="{ background: slide.bg }">
          <div class="slide-overlay"></div>
          <div class="slide-text container">
            <h2 class="slide-title">{{ slide.title }}</h2>
            <p class="slide-desc">{{ slide.desc }}</p>
          </div>
        </div>
      </div>
    </div>
    <div class="banner-dots">
      <button
        v-for="(_, index) in slides"
        :key="index"
        class="dot"
        :class="{ active: currentIndex === index }"
        @click="currentIndex = index"
      />
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted } from 'vue'

const slides = [
  {
    title: '编辑大模型',
    desc: 'AI 审校硬核黑科技，精准核查多维度编校问题',
    bg: 'linear-gradient(135deg, #5eb3e8 0%, #87c9f0 50%, #b3ddf5 100%)'
  },
  {
    title: '智校云雠',
    desc: '智能审校利器，全方位覆盖四大审校维度',
    bg: 'linear-gradient(135deg, #3a9fd4 0%, #5eb3e8 50%, #87c9f0 100%)'
  }
]

const currentIndex = ref(0)

onMounted(() => {
  setInterval(() => {
    currentIndex.value = (currentIndex.value + 1) % slides.length
  }, 6000)
})
</script>

<style scoped>
.app-banner {
  position: relative;
  height: 420px;
  border-radius: var(--radius-xl);
  overflow: hidden;
  margin: 0 24px 24px;
  box-shadow: var(--shadow-lg);
}

.slide {
  position: absolute;
  inset: 0;
  opacity: 0;
  transition: opacity 0.8s ease;
}

.slide.active {
  opacity: 1;
  z-index: 1;
}

.slide-content {
  height: 100%;
  background-size: cover;
  background-position: center;
  position: relative;
}

.slide-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, rgba(94, 179, 232, 0.4) 0%, rgba(232, 244, 252, 0.7) 100%);
}

.slide-text {
  position: relative;
  z-index: 2;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.slide-title {
  font-size: 42px;
  color: white;
  text-shadow: 0 2px 12px rgba(0,0,0,0.2);
  margin-bottom: 16px;
}

.slide-desc {
  font-size: 20px;
  color: rgba(255,255,255,0.95);
}

.banner-dots {
  position: absolute;
  bottom: 24px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  gap: 12px;
  z-index: 10;
}

.dot {
  width: 12px;
  height: 12px;
  border-radius: var(--radius-full);
  border: 2px solid white;
  background: transparent;
  cursor: pointer;
  transition: all var(--transition-fast);
}

.dot.active {
  background: white;
  transform: scale(1.2);
}
</style>

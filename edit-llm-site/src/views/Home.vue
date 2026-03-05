<template>
  <div class="home-page">
    <AppHeader />
    <AppNav />
    <main class="main-content">
      <AppBanner />
      <ProductSection
        title="编辑大模型"
        description="编辑大模型，AI 审校硬核黑科技！核心技术 + 专业知识库，精准核查多维度编校问题，一键输出修正润色方案，破解行业痛点，强势赋能出版数智化转型。"
        icon="🤖"
        link="https://aep.hep.com.cn/proofread/index"
      />
      <ProductSection
        title="智校云雠"
        description="智能审校利器智校云雠，全方位覆盖字符、逻辑、知识、格式四大审校维度，以智能科技深度赋能编辑工作，革新审校效率、重塑工作体验，强力驱动出版行业高质量进阶发展。"
        icon="☁️"
        link="#"
        :reverse="true"
      />
      <TabSection />
      <ApplySection />
    </main>
    <AppFooter />
  </div>
</template>

<script setup>
import AppHeader from '../components/AppHeader.vue'
import AppNav from '../components/AppNav.vue'
import AppBanner from '../components/AppBanner.vue'
import ProductSection from '../components/ProductSection.vue'
import TabSection from '../components/TabSection.vue'
import ApplySection from '../components/ApplySection.vue'
import AppFooter from '../components/AppFooter.vue'
</script>

<style scoped>
.home-page {
  min-height: 100vh;
}

.main-content {
  padding-bottom: 0;
}
</style>

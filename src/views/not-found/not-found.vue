<template>
  <div class="not-found-content">
    <h1>404</h1>
    <blockquote><p>糟糕！这个页面不存在。</p></blockquote>
    <el-link type="primary" :underline="false" @click="goHome"
      >返回主页。</el-link
    >
  </div>
</template>

<script lang="ts" setup>
import { useRouter } from 'vue-router'
const router = useRouter()
const goHome = () => {
  router.push('/')
}
</script>

<style scoped>
.not-found-content {
  max-width: 740px;
  margin: 0 auto;
  padding: 2rem 2.5rem;
}
h1 {
  padding-top: 4.6rem;
  font-size: 34px;
  font-weight: bold;
}
blockquote {
  font-size: 1rem;
  color: #999;
  border-left: 0.2rem solid #dfe2e5;
  margin: 1rem 0;
  padding: 0.25rem 0 0.25rem 1rem;
}
.el-link {
  font-size: 16px;
}
</style>

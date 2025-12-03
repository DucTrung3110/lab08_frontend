<template>
  <div class="container">
    <div class="row">
      <div class="col-md-8 mx-auto">
        <h1 class="mb-5 text-center animate-fade-in">Lợi ích khi sử dụng Nuxt.js</h1>

        <div class="row">
          <div v-for="(benefit, index) in benefits" :key="index" class="col-md-6 mb-4">
            <div class="benefit-card" :style="{ animationDelay: `${index * 0.1}s` }">
              <div class="benefit-icon">{{ benefit.icon }}</div>
              <h5 class="benefit-title">{{ benefit.title }}</h5>
              <p class="benefit-description">{{ benefit.description }}</p>
            </div>
          </div>
        </div>

        <div class="mt-5 p-5 summary-box">
          <h4 class="mb-4 text-center">Tóm tắt</h4>
          <p class="lead text-center">
            Nuxt.js là một framework hoàn chỉnh giúp bạn xây dựng các ứng dụng web hiện đại 
            với hiệu suất cao, SEO tốt và developer experience tuyệt vời.
          </p>
          <div class="stats-row">
            <div class="stat">
              <div class="stat-number">98%</div>
              <div class="stat-label">Lighthouse Score</div>
            </div>
            <div class="stat">
              <div class="stat-number">2ms</div>
              <div class="stat-label">Load Time</div>
            </div>
            <div class="stat">
              <div class="stat-number">100%</div>
              <div class="stat-label">SEO Ready</div>
            </div>
          </div>
        </div>

        <div class="mt-5 text-center">
          <NuxtLink to="/" class="btn btn-outline-primary me-2">← Trang chủ</NuxtLink>
          <NuxtLink to="/about" class="btn btn-outline-info">So sánh →</NuxtLink>
          <NuxtLink to="/contact" class="btn btn-outline-success ms-2">Liên hệ →</NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

definePageMeta({
  title: 'Lợi ích của Nuxt.js'
})

const benefits = ref([
  {
    icon: '🚀',
    title: 'SSR & CSR',
    description: 'Hỗ trợ cả Server-Side Rendering và Client-Side Rendering cho hiệu suất tối ưu.'
  },
  {
    icon: '📁',
    title: 'Routing Tự động',
    description: 'Quản lý routing tự động thông qua hệ thống Pages - không cần cấu hình thủ công.'
  },
  {
    icon: '🎯',
    title: 'Quản lý trạng thái',
    description: 'Tích hợp dễ dàng với Vuex hoặc Pinia cho quản lý trạng thái hiệu quả.'
  },
  {
    icon: '🔍',
    title: 'SEO Tốt',
    description: 'Hỗ trợ SEO tốt hơn nhờ Server-Side Rendering giúp bots indexing tốt hơn.'
  },
  {
    icon: '⚙️',
    title: 'Cấu hình dễ dàng',
    description: 'Quản lý cấu hình đơn giản với các modules có sẵn, tiết kiệm thời gian setup.'
  },
  {
    icon: '📦',
    title: 'Middleware',
    description: 'Hỗ trợ middleware cho phép kiểm soát truy cập và xử lý dữ liệu trước render.'
  },
  {
    icon: '📝',
    title: 'Layouts',
    description: 'Hệ thống layouts giúp tái sử dụng code và duy trì consistency trong ứng dụng.'
  },
  {
    icon: '🔌',
    title: 'Plugin System',
    description: 'Plugin system cho phép mở rộng functionality và tích hợp thư viện bên thứ ba.'
  }
])
</script>

<style scoped>
h1 {
  color: #003366;
  font-weight: bold;
}

.animate-fade-in {
  animation: fadeInDown 0.6s ease-out;
}

.benefit-card {
  background: white;
  border-left: 4px solid #667eea;
  padding: 25px;
  border-radius: 8px;
  transition: all 0.3s ease;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
  height: 100%;
  animation: fadeInUp 0.5s ease-out forwards;
  opacity: 0;
}

.benefit-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.15);
  border-left-color: #764ba2;
}

.benefit-icon {
  font-size: 2.5rem;
  margin-bottom: 15px;
}

.benefit-title {
  color: #003366;
  font-weight: 600;
  margin-bottom: 10px;
}

.benefit-description {
  color: #666;
  font-size: 0.95rem;
  margin: 0;
  line-height: 1.5;
}

.summary-box {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  border-radius: 10px;
  animation: fadeInUp 0.6s ease-out 0.8s both;
}

.summary-box h4 {
  color: white;
  font-weight: 700;
}

.summary-box .lead {
  color: rgba(255, 255, 255, 0.95);
  font-size: 1.1rem;
}

.stats-row {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 20px;
  margin-top: 30px;
}

.stat {
  text-align: center;
  padding: 20px;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  border-radius: 8px;
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.stat-number {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 10px;
}

.stat-label {
  font-size: 0.9rem;
  opacity: 0.9;
}

.btn-outline-primary {
  color: #667eea;
  border-color: #667eea;
}

.btn-outline-primary:hover {
  background: #667eea;
  border-color: #667eea;
}

.btn-outline-info {
  color: #17a2b8;
  border-color: #17a2b8;
}

.btn-outline-info:hover {
  background: #17a2b8;
  border-color: #17a2b8;
}

.btn-outline-success {
  color: #28a745;
  border-color: #28a745;
}

.btn-outline-success:hover {
  background: #28a745;
  border-color: #28a745;
}

@keyframes fadeInDown {
  from {
    opacity: 0;
    transform: translateY(-20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 768px) {
  .stats-row {
    grid-template-columns: 1fr;
  }

  .summary-box {
    padding: 30px 15px;
  }
}
</style>

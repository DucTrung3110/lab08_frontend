<template>
  <div class="container">
    <div class="row">
      <div class="col-md-10 mx-auto">
        <h1 class="mb-4 text-center animate-fade-in">So sánh Nuxt.js và Vue.js</h1>
        
        <div class="table-responsive">
          <table class="table table-striped table-hover comparison-table">
            <thead class="table-dark">
              <tr>
                <th>Tiêu chí</th>
                <th class="text-center">Nuxt.js</th>
                <th class="text-center">Vue.js</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="(item, index) in comparisonData" :key="index" :style="{ animationDelay: `${index * 0.1}s` }" class="animate-row">
                <td><strong>{{ item.criteria }}</strong></td>
                <td class="text-center"><span :class="item.nuxtBadge">{{ item.nuxt }}</span></td>
                <td class="text-center"><span :class="item.vueBadge">{{ item.vue }}</span></td>
              </tr>
            </tbody>
          </table>
        </div>

        <div class="mt-5 p-4 bg-light rounded comparison-info">
          <h5 class="mb-3">Khi nào sử dụng Nuxt.js?</h5>
          <ul class="fa-ul">
            <li><span class="fa-li">✓</span>Khi cần SSR hoặc Static Site Generation</li>
            <li><span class="fa-li">✓</span>Khi cần routing tự động</li>
            <li><span class="fa-li">✓</span>Khi cần tối ưu SEO</li>
            <li><span class="fa-li">✓</span>Khi xây dựng ứng dụng lớn, phức tạp</li>
          </ul>

          <hr>

          <h5 class="mb-3">Khi nào sử dụng Vue.js?</h5>
          <ul class="fa-ul">
            <li><span class="fa-li">✓</span>Khi xây dựng SPA đơn giản</li>
            <li><span class="fa-li">✓</span>Khi muốn kiểm soát toàn bộ cấu trúc</li>
            <li><span class="fa-li">✓</span>Khi learning/prototype</li>
            <li><span class="fa-li">✓</span>Khi không cần SSR</li>
          </ul>
        </div>

        <div class="mt-5 text-center">
          <NuxtLink to="/" class="btn btn-outline-primary me-2">← Trở về trang chủ</NuxtLink>
          <NuxtLink to="/benefits" class="btn btn-outline-success">Xem lợi ích →</NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

definePageMeta({
  title: 'So sánh Nuxt.js vs Vue.js'
})

const comparisonData = ref([
  {
    criteria: 'Rendering',
    nuxt: 'SSR + CSR',
    nuxtBadge: 'badge bg-success',
    vue: 'CSR',
    vueBadge: 'badge bg-info'
  },
  {
    criteria: 'Routing',
    nuxt: 'Tự động qua Pages',
    nuxtBadge: 'badge bg-success',
    vue: 'Cần cấu hình thủ công',
    vueBadge: 'badge bg-warning'
  },
  {
    criteria: 'Quản lý trạng thái',
    nuxt: 'Tích hợp dễ dàng',
    nuxtBadge: 'badge bg-success',
    vue: 'Cần cấu hình thêm',
    vueBadge: 'badge bg-warning'
  },
  {
    criteria: 'SEO',
    nuxt: 'Tốt hơn (SSR)',
    nuxtBadge: 'badge bg-success',
    vue: 'Cần tối ưu',
    vueBadge: 'badge bg-info'
  },
  {
    criteria: 'Độ phức tạp',
    nuxt: 'Trung bình',
    nuxtBadge: 'badge bg-warning',
    vue: 'Đơn giản',
    vueBadge: 'badge bg-info'
  },
  {
    criteria: 'Tối ưu hóa',
    nuxt: 'Built-in',
    nuxtBadge: 'badge bg-success',
    vue: 'Thủ công',
    vueBadge: 'badge bg-info'
  },
  {
    criteria: 'Auto Import',
    nuxt: 'Có',
    nuxtBadge: 'badge bg-success',
    vue: 'Không',
    vueBadge: 'badge bg-danger'
  },
  {
    criteria: 'Middleware',
    nuxt: 'Có hỗ trợ',
    nuxtBadge: 'badge bg-success',
    vue: 'Cần thêm module',
    vueBadge: 'badge bg-warning'
  }
])
</script>

<style scoped>
h1 {
  color: #003366;
  font-weight: bold;
  margin-bottom: 40px;
}

.comparison-table {
  margin-bottom: 0;
}

.comparison-table th,
.comparison-table td {
  vertical-align: middle;
}

.comparison-table .badge {
  padding: 8px 12px;
  font-size: 0.85rem;
  font-weight: 500;
}

.table-hover tbody tr {
  transition: background-color 0.3s ease;
}

.table-hover tbody tr:hover {
  background-color: #f5f5f5 !important;
}

.animate-fade-in {
  animation: fadeInDown 0.6s ease-out;
}

.animate-row {
  animation: fadeInUp 0.5s ease-out forwards;
  opacity: 0;
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
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.comparison-info {
  border-left: 4px solid #667eea;
  background: #f8f9fa;
}

.comparison-info h5 {
  color: #003366;
  font-weight: 600;
}

.fa-ul li {
  color: #555;
  margin-bottom: 10px;
}

.btn-outline-primary {
  color: #667eea;
  border-color: #667eea;
}

.btn-outline-primary:hover {
  background: #667eea;
  border-color: #667eea;
}

.btn-outline-success {
  color: #28a745;
  border-color: #28a745;
}

.btn-outline-success:hover {
  background: #28a745;
  border-color: #28a745;
}

@media (max-width: 768px) {
  .comparison-table {
    font-size: 0.9rem;
  }

  .comparison-table .badge {
    font-size: 0.75rem;
    padding: 5px 8px;
  }
}
</style>

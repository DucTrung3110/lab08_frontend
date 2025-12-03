<template>
  <div class="container">
    <div class="row">
      <div class="col-md-8 mx-auto">
        <h1 class="mb-4 text-center">Giới thiệu về Nuxt.js</h1>
        <div class="card">
          <div class="card-body">
            <p class="lead">
              Nuxt.js là một framework mạnh mẽ cho Vue.js, giúp phát triển ứng dụng SSR (Server-Side Rendering) 
              và SPA (Single Page Application) một cách dễ dàng.
            </p>
            <p>
              Nuxt.js được xây dựng trên nền tảng Vue.js và cung cấp nhiều tính năng nâng cao như:
            </p>
            <ul class="list-group list-group-flush">
              <li class="list-group-item">🚀 Hỗ trợ SSR và CSR cho hiệu suất tối ưu</li>
              <li class="list-group-item">📁 Quản lý routing tự động thông qua hệ thống Pages</li>
              <li class="list-group-item">🎯 Tích hợp dễ dàng với Vuex cho quản lý trạng thái</li>
              <li class="list-group-item">🔍 Hỗ trợ SEO tốt hơn nhờ SSR</li>
              <li class="list-group-item">⚙️ Quản lý cấu hình đơn giản với các modules có sẵn</li>
            </ul>

            <div class="mt-4">
              <p>Hãy tìm hiểu thêm về:</p>
              <div class="btn-group" role="group">
                <NuxtLink to="/about" class="btn btn-primary">So sánh Nuxt.js và Vue.js</NuxtLink>
                <NuxtLink to="/benefits" class="btn btn-success">Lợi ích của Nuxt.js</NuxtLink>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  title: 'Trang chủ - Nuxt.js'
})
</script>

<style scoped>
h1 {
  color: #003366;
  font-weight: bold;
}

.card {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
}

.btn-group {
  gap: 10px;
}
</style>

<template>
  <div>
    <!-- Hero Section -->
    <section class="hero-section mb-5">
      <div class="container py-5">
        <div class="row align-items-center">
          <div class="col-lg-6 mb-4 mb-lg-0">
            <h1 class="display-4 fw-bold mb-4 animate-fade-in">
              Chào mừng đến với <span class="text-primary">Nuxt.js</span> Lab 8
            </h1>
            <p class="lead mb-4">
              Khám phá framework Vue.js tiên tiến giúp bạn xây dựng ứng dụng web hiện đại với SSR, routing tự động, và nhiều tính năng mạnh mẽ khác.
            </p>
            <div class="btn-group" role="group">
              <NuxtLink to="/about" class="btn btn-primary btn-lg">Tìm hiểu thêm</NuxtLink>
              <NuxtLink to="/benefits" class="btn btn-outline-primary btn-lg">Xem lợi ích</NuxtLink>
            </div>
          </div>
          <div class="col-lg-6">
            <div class="hero-image">
              <div class="feature-card">
                <div class="feature-icon">⚡</div>
                <div class="feature-text">Hiệu suất cao</div>
              </div>
              <div class="feature-card">
                <div class="feature-icon">🎯</div>
                <div class="feature-text">Routing tự động</div>
              </div>
              <div class="feature-card">
                <div class="feature-icon">🔍</div>
                <div class="feature-text">SEO tốt</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section class="features-section mb-5">
      <div class="container">
        <h2 class="text-center mb-5">Tại sao chọn Nuxt.js?</h2>
        <div class="row">
          <div class="col-md-4 mb-4">
            <div class="feature-box">
              <div class="feature-box-icon">📦</div>
              <h5>Công cụ toàn bộ</h5>
              <p>Nuxt.js cung cấp tất cả những gì bạn cần để xây dựng ứng dụng web hiện đại, từ routing đến middleware.</p>
            </div>
          </div>
          <div class="col-md-4 mb-4">
            <div class="feature-box">
              <div class="feature-box-icon">⚙️</div>
              <h5>Cấu hình dễ dàng</h5>
              <p>Không cần cấu hình phức tạp - Nuxt.js tự động xử lý routing dựa trên cấu trúc thư mục.</p>
            </div>
          </div>
          <div class="col-md-4 mb-4">
            <div class="feature-box">
              <div class="feature-box-icon">🚀</div>
              <h5>Triển khai nhanh</h5>
              <p>Dễ dàng triển khai lên Netlify, Vercel hoặc các nền tảng cloud khác chỉ với một click.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Info Section -->
    <section class="info-section">
      <div class="container">
        <div class="row">
          <div class="col-md-8 mx-auto">
            <h2 class="mb-4 text-center">Nội dung Nuxt.js</h2>
            <p class="lead mb-3">
              Nuxt.js là một framework mạnh mẽ cho Vue.js, giúp phát triển ứng dụng SSR (Server-Side Rendering) 
              và SPA (Single Page Application) một cách dễ dàng.
            </p>
            <p>
              Hãy tìm hiểu thêm về:
            </p>
            <ul class="list-group list-group-flush">
              <li class="list-group-item">🚀 Hỗ trợ SSR và CSR cho hiệu suất tối ưu</li>
              <li class="list-group-item">📁 Quản lý routing tự động thông qua hệ thống Pages</li>
              <li class="list-group-item">🎯 Tích hợp dễ dàng với Vuex cho quản lý trạng thái</li>
              <li class="list-group-item">🔍 Hỗ trợ SEO tốt hơn nhờ SSR</li>
              <li class="list-group-item">⚙️ Quản lý cấu hình đơn giản với các modules có sẵn</li>
            </ul>

            <div class="mt-5 text-center">
              <NuxtLink to="/about" class="btn btn-primary me-2">So sánh Nuxt.js và Vue.js</NuxtLink>
              <NuxtLink to="/benefits" class="btn btn-success">Lợi ích của Nuxt.js</NuxtLink>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
definePageMeta({
  title: 'Trang chủ - Nuxt.js Lab 8'
})
</script>

<style scoped>
.hero-section {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  border-radius: 10px;
  overflow: hidden;
}

.hero-section h1 {
  color: white;
  animation: fadeInUp 0.8s ease-out;
}

.hero-section .lead {
  font-size: 1.1rem;
  opacity: 0.95;
  animation: fadeInUp 0.8s ease-out 0.2s both;
}

.hero-section .btn-group {
  gap: 10px;
  animation: fadeInUp 0.8s ease-out 0.4s both;
}

.btn-primary {
  background: #ffffff;
  color: #667eea;
  border: none;
}

.btn-primary:hover {
  background: #f0f0f0;
  color: #667eea;
}

.btn-outline-primary {
  color: white;
  border-color: white;
}

.btn-outline-primary:hover {
  background: white;
  color: #667eea;
}

.hero-image {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 15px;
  perspective: 1000px;
}

.feature-card {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  padding: 20px;
  border-radius: 10px;
  border: 1px solid rgba(255, 255, 255, 0.2);
  text-align: center;
  color: white;
  transition: transform 0.3s ease;
}

.feature-card:hover {
  transform: translateY(-10px);
}

.feature-icon {
  font-size: 2.5rem;
  margin-bottom: 10px;
}

.feature-text {
  font-weight: 600;
}

.features-section {
  padding: 40px 0;
}

.feature-box {
  background: #f8f9fa;
  padding: 30px;
  border-radius: 10px;
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  height: 100%;
}

.feature-box:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.feature-box-icon {
  font-size: 3rem;
  margin-bottom: 15px;
}

.feature-box h5 {
  color: #333;
  font-weight: 600;
  margin-bottom: 15px;
}

.feature-box p {
  color: #666;
  font-size: 0.95rem;
}

.info-section {
  padding: 40px 0;
}

.list-group-item {
  border-left: 3px solid #667eea;
  padding-left: 15px;
}

h2 {
  color: #333;
  font-weight: 700;
  margin-bottom: 30px;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade-in {
  animation: fadeInUp 0.8s ease-out;
}

@media (max-width: 768px) {
  .hero-section {
    margin: 0 -12px;
  }

  .hero-image {
    grid-template-columns: 1fr;
    margin-top: 30px;
  }

  .feature-card {
    grid-column: span 1;
  }
}
</style>

<template>
  <div class="container">
    <div class="row">
      <div class="col-md-8 mx-auto">
        <h1 class="mb-4 text-center">Lợi ích khi sử dụng Nuxt.js</h1>

        <div class="row">
          <div class="col-md-6 mb-4">
            <div class="card h-100">
              <div class="card-body">
                <h5 class="card-title">🚀 SSR & CSR</h5>
                <p class="card-text">
                  Hỗ trợ cả Server-Side Rendering và Client-Side Rendering cho hiệu suất tối ưu.
                </p>
              </div>
            </div>
          </div>

          <div class="col-md-6 mb-4">
            <div class="card h-100">
              <div class="card-body">
                <h5 class="card-title">📁 Routing Tự động</h5>
                <p class="card-text">
                  Quản lý routing tự động thông qua hệ thống Pages - không cần cấu hình thủ công.
                </p>
              </div>
            </div>
          </div>

          <div class="col-md-6 mb-4">
            <div class="card h-100">
              <div class="card-body">
                <h5 class="card-title">🎯 Quản lý trạng thái</h5>
                <p class="card-text">
                  Tích hợp dễ dàng với Vuex hoặc Pinia cho quản lý trạng thái hiệu quả.
                </p>
              </div>
            </div>
          </div>

          <div class="col-md-6 mb-4">
            <div class="card h-100">
              <div class="card-body">
                <h5 class="card-title">🔍 SEO Tốt</h5>
                <p class="card-text">
                  Hỗ trợ SEO tốt hơn nhờ Server-Side Rendering giúp bots indexing tốt hơn.
                </p>
              </div>
            </div>
          </div>

          <div class="col-md-6 mb-4">
            <div class="card h-100">
              <div class="card-body">
                <h5 class="card-title">⚙️ Cấu hình dễ dàng</h5>
                <p class="card-text">
                  Quản lý cấu hình đơn giản với các modules có sẵn, tiết kiệm thời gian setup.
                </p>
              </div>
            </div>
          </div>

          <div class="col-md-6 mb-4">
            <div class="card h-100">
              <div class="card-body">
                <h5 class="card-title">📦 Middleware</h5>
                <p class="card-text">
                  Hỗ trợ middleware cho phép kiểm soát truy cập và xử lý dữ liệu trước render.
                </p>
              </div>
            </div>
          </div>

          <div class="col-md-6 mb-4">
            <div class="card h-100">
              <div class="card-body">
                <h5 class="card-title">📝 Layouts</h5>
                <p class="card-text">
                  Hệ thống layouts giúp tái sử dụng code và duy trì consistency trong ứng dụng.
                </p>
              </div>
            </div>
          </div>

          <div class="col-md-6 mb-4">
            <div class="card h-100">
              <div class="card-body">
                <h5 class="card-title">🔌 Plugin System</h5>
                <p class="card-text">
                  Plugin system cho phép mở rộng functionality và tích hợp thư viện bên thứ ba.
                </p>
              </div>
            </div>
          </div>
        </div>

        <div class="mt-5 p-4 bg-light rounded text-center">
          <h4>Tóm tắt</h4>
          <p class="lead">
            Nuxt.js là một framework hoàn chỉnh giúp bạn xây dựng các ứng dụng web hiện đại 
            với hiệu suất cao, SEO tốt và developer experience tuyệt vời.
          </p>
        </div>

        <div class="mt-4 text-center">
          <NuxtLink to="/" class="btn btn-outline-primary me-2">← Trang chủ</NuxtLink>
          <NuxtLink to="/about" class="btn btn-outline-info">So sánh →</NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  title: 'Lợi ích của Nuxt.js'
})
</script>

<style scoped>
h1 {
  color: #003366;
  font-weight: bold;
}

.card {
  border-left: 4px solid #003366;
  transition: transform 0.2s, box-shadow 0.2s;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15);
}

.card-title {
  color: #003366;
  font-weight: bold;
}
</style>

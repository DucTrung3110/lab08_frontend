<template>
  <div class="container">
    <div class="row">
      <div class="col-md-10 mx-auto">
        <h1 class="mb-4 text-center">So sánh Nuxt.js và Vue.js</h1>
        
        <div class="table-responsive">
          <table class="table table-striped table-hover">
            <thead class="table-dark">
              <tr>
                <th>Tiêu chí</th>
                <th>Nuxt.js</th>
                <th>Vue.js</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td><strong>Rendering</strong></td>
                <td><span class="badge bg-success">SSR + CSR</span></td>
                <td><span class="badge bg-info">CSR</span></td>
              </tr>
              <tr>
                <td><strong>Routing</strong></td>
                <td><span class="badge bg-success">Tự động qua Pages</span></td>
                <td><span class="badge bg-warning">Cần cấu hình thủ công</span></td>
              </tr>
              <tr>
                <td><strong>Quản lý trạng thái</strong></td>
                <td><span class="badge bg-success">Tích hợp dễ dàng</span></td>
                <td><span class="badge bg-warning">Cần cấu hình thêm</span></td>
              </tr>
              <tr>
                <td><strong>SEO</strong></td>
                <td><span class="badge bg-success">Tốt hơn (SSR)</span></td>
                <td><span class="badge bg-info">Cần tối ưu</span></td>
              </tr>
              <tr>
                <td><strong>Độ phức tạp</strong></td>
                <td><span class="badge bg-warning">Trung bình</span></td>
                <td><span class="badge bg-info">Đơn giản</span></td>
              </tr>
              <tr>
                <td><strong>Tối ưu hóa</strong></td>
                <td><span class="badge bg-success">Built-in</span></td>
                <td><span class="badge bg-info">Thủ công</span></td>
              </tr>
            </tbody>
          </table>
        </div>

        <div class="mt-4 p-4 bg-light rounded">
          <h5>Khi nào sử dụng Nuxt.js?</h5>
          <ul>
            <li>Khi cần SSR hoặc Static Site Generation</li>
            <li>Khi cần routing tự động</li>
            <li>Khi cần tối ưu SEO</li>
            <li>Khi xây dựng ứng dụng lớn, phức tạp</li>
          </ul>

          <h5 class="mt-3">Khi nào sử dụng Vue.js?</h5>
          <ul>
            <li>Khi xây dựng SPA đơn giản</li>
            <li>Khi muốn kiểm soát toàn bộ cấu trúc</li>
            <li>Khi learning/prototype</li>
            <li>Khi không cần SSR</li>
          </ul>
        </div>

        <div class="mt-4 text-center">
          <NuxtLink to="/" class="btn btn-outline-primary me-2">← Trở về trang chủ</NuxtLink>
          <NuxtLink to="/benefits" class="btn btn-outline-success">Xem lợi ích →</NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  title: 'So sánh Nuxt.js vs Vue.js'
})
</script>

<style scoped>
h1 {
  color: #003366;
  font-weight: bold;
}

table {
  margin-bottom: 0;
}

.table-hover tbody tr:hover {
  background-color: #f5f5f5;
}
</style>

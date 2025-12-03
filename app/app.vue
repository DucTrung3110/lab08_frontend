<template>
  <div :class="{ 'dark-mode': isDarkMode }">
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark sticky-top">
      <div class="container">
        <NuxtLink to="/" class="navbar-brand fw-bold">
          <span class="text-primary">Nuxt</span>.js Lab 8
        </NuxtLink>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item">
              <NuxtLink to="/" class="nav-link">Trang chủ</NuxtLink>
            </li>
            <li class="nav-item">
              <NuxtLink to="/about" class="nav-link">So sánh</NuxtLink>
            </li>
            <li class="nav-item">
              <NuxtLink to="/benefits" class="nav-link">Lợi ích</NuxtLink>
            </li>
            <li class="nav-item">
              <NuxtLink to="/contact" class="nav-link">Liên hệ</NuxtLink>
            </li>
            <li class="nav-item ms-2">
              <button @click="toggleDarkMode" class="btn btn-sm btn-outline-light">
                {{ isDarkMode ? '☀️' : '🌙' }}
              </button>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <main class="py-5">
      <NuxtPage />
    </main>

    <footer class="bg-dark text-light py-5 mt-5">
      <div class="container">
        <div class="row">
          <div class="col-md-4 mb-4">
            <h5 class="mb-3">Về Nuxt.js Lab 8</h5>
            <p>Dự án học tập về Nuxt.js, Vue.js Framework hiện đại cho phát triển web.</p>
          </div>
          <div class="col-md-4 mb-4">
            <h5 class="mb-3">Liên kết nhanh</h5>
            <ul class="list-unstyled">
              <li><NuxtLink to="/" class="text-light text-decoration-none">Trang chủ</NuxtLink></li>
              <li><NuxtLink to="/about" class="text-light text-decoration-none">So sánh</NuxtLink></li>
              <li><NuxtLink to="/benefits" class="text-light text-decoration-none">Lợi ích</NuxtLink></li>
              <li><NuxtLink to="/contact" class="text-light text-decoration-none">Liên hệ</NuxtLink></li>
            </ul>
          </div>
          <div class="col-md-4 mb-4">
            <h5 class="mb-3">Thông tin</h5>
            <p>
              <strong>Email:</strong> student@example.com<br>
              <strong>Phone:</strong> +84 123 456 789<br>
              <strong>GitHub:</strong> <a href="https://github.com/DucTrung3110/lab08_frontend" target="_blank" class="text-light">lab08_frontend</a>
            </p>
          </div>
        </div>
        <hr class="bg-light">
        <div class="text-center">
          <p class="mb-0">&copy; 2025 Nuxt.js Lab 8. All rights reserved.</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const isDarkMode = ref(false)

const toggleDarkMode = () => {
  isDarkMode.value = !isDarkMode.value
  if (isDarkMode.value) {
    document.documentElement.style.colorScheme = 'dark'
  } else {
    document.documentElement.style.colorScheme = 'light'
  }
}
</script>

<style scoped>
:global(.dark-mode) {
  --bs-bg-rgb: 33, 37, 41;
  --bs-body-bg-rgb: 33, 37, 41;
  --bs-body-color-rgb: 255, 255, 255;
}

:global(.dark-mode body) {
  background-color: #212529;
  color: #ffffff;
}

:global(.dark-mode .card) {
  background-color: #343a40;
  color: #ffffff;
  border-color: #495057;
}

:global(.dark-mode .table) {
  color: #ffffff;
}

:global(.dark-mode .table-dark) {
  background-color: #495057;
}

:global(.dark-mode .table-striped tbody tr:nth-of-type(odd)) {
  background-color: #343a40;
}

main {
  min-height: calc(100vh - 56px - 400px);
}

.navbar-brand {
  font-size: 1.5rem;
}

.sticky-top {
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

footer {
  margin-top: auto;
}

footer a:hover {
  text-decoration: underline !important;
}
</style>

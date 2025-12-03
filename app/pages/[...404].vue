<template>
  <div class="error-page">
    <div class="container">
      <div class="error-content">
        <div class="error-code">404</div>
        <h1 class="error-title">Trang không tìm thấy</h1>
        <p class="error-message">
          Xin lỗi, trang bạn đang tìm kiếm không tồn tại hoặc đã bị xóa.
        </p>

        <div class="suggestions">
          <p class="suggestion-title">Có thể bạn đang tìm:</p>
          <div class="suggestion-links">
            <NuxtLink to="/" class="suggestion-link">
              <span class="icon">🏠</span>
              <span class="text">Trang chủ</span>
            </NuxtLink>
            <NuxtLink to="/about" class="suggestion-link">
              <span class="icon">📚</span>
              <span class="text">So sánh</span>
            </NuxtLink>
            <NuxtLink to="/benefits" class="suggestion-link">
              <span class="icon">⭐</span>
              <span class="text">Lợi ích</span>
            </NuxtLink>
            <NuxtLink to="/contact" class="suggestion-link">
              <span class="icon">📧</span>
              <span class="text">Liên hệ</span>
            </NuxtLink>
          </div>
        </div>

        <button @click="goBack" class="btn btn-primary btn-lg mt-4">
          ← Quay lại trang trước
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
const goBack = () => {
  if (window.history.length > 1) {
    window.history.back()
  } else {
    navigateTo('/')
  }
}
</script>

<style scoped>
.error-page {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
}

.error-content {
  text-align: center;
  animation: fadeIn 0.6s ease-out;
}

.error-code {
  font-size: 120px;
  font-weight: 900;
  margin: 0;
  text-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
  animation: bounce 1s ease-out;
}

.error-title {
  font-size: 2.5rem;
  font-weight: 700;
  margin: 20px 0;
  animation: fadeInUp 0.8s ease-out 0.2s both;
}

.error-message {
  font-size: 1.1rem;
  opacity: 0.95;
  margin-bottom: 40px;
  animation: fadeInUp 0.8s ease-out 0.4s both;
}

.suggestions {
  margin: 50px 0;
  animation: fadeInUp 0.8s ease-out 0.6s both;
}

.suggestion-title {
  font-size: 1.1rem;
  margin-bottom: 20px;
  font-weight: 600;
}

.suggestion-links {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
  gap: 15px;
  max-width: 500px;
  margin: 0 auto;
}

.suggestion-link {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 20px;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  border-radius: 10px;
  color: white;
  text-decoration: none;
  transition: all 0.3s ease;
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.suggestion-link:hover {
  background: rgba(255, 255, 255, 0.2);
  transform: translateY(-5px);
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
}

.icon {
  font-size: 2rem;
  margin-bottom: 8px;
}

.text {
  font-size: 0.9rem;
  font-weight: 500;
}

.btn {
  animation: fadeInUp 0.8s ease-out 0.8s both;
}

.btn-primary {
  background: white;
  color: #667eea;
  border: none;
  font-weight: 600;
  padding: 12px 30px;
  font-size: 1rem;
}

.btn-primary:hover {
  background: #f0f0f0;
  color: #667eea;
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
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

@keyframes bounce {
  0%, 100% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.05);
  }
}

@media (max-width: 768px) {
  .error-code {
    font-size: 80px;
  }

  .error-title {
    font-size: 2rem;
  }

  .suggestion-links {
    grid-template-columns: repeat(2, 1fr);
  }
}
</style>

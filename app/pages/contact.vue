<template>
  <div class="container">
    <div class="row">
      <div class="col-md-8 mx-auto">
        <h1 class="mb-4 text-center">Liên hệ với chúng tôi</h1>

        <div class="row mb-5">
          <div class="col-md-4 mb-4">
            <div class="contact-box">
              <div class="contact-icon">📧</div>
              <h5>Email</h5>
              <p>
                <a href="mailto:student@example.com">student@example.com</a>
              </p>
            </div>
          </div>
          <div class="col-md-4 mb-4">
            <div class="contact-box">
              <div class="contact-icon">📞</div>
              <h5>Điện thoại</h5>
              <p>
                <a href="tel:+84123456789">+84 123 456 789</a>
              </p>
            </div>
          </div>
          <div class="col-md-4 mb-4">
            <div class="contact-box">
              <div class="contact-icon">🏢</div>
              <h5>Địa chỉ</h5>
              <p>
                123 Đường Lê Lợi<br>
                Quận 1, TP. HCM
              </p>
            </div>
          </div>
        </div>

        <div class="card shadow-lg">
          <div class="card-body p-4">
            <h4 class="mb-4">Gửi tin nhắn cho chúng tôi</h4>
            <form @submit.prevent="submitForm">
              <div class="mb-3">
                <label for="name" class="form-label">Họ và tên</label>
                <input
                  v-model="form.name"
                  type="text"
                  class="form-control"
                  id="name"
                  placeholder="Nhập tên của bạn"
                  required
                >
              </div>

              <div class="mb-3">
                <label for="email" class="form-label">Email</label>
                <input
                  v-model="form.email"
                  type="email"
                  class="form-control"
                  id="email"
                  placeholder="Nhập email của bạn"
                  required
                >
              </div>

              <div class="mb-3">
                <label for="phone" class="form-label">Số điện thoại</label>
                <input
                  v-model="form.phone"
                  type="tel"
                  class="form-control"
                  id="phone"
                  placeholder="Nhập số điện thoại"
                >
              </div>

              <div class="mb-3">
                <label for="subject" class="form-label">Tiêu đề</label>
                <input
                  v-model="form.subject"
                  type="text"
                  class="form-control"
                  id="subject"
                  placeholder="Tiêu đề tin nhắn"
                  required
                >
              </div>

              <div class="mb-3">
                <label for="message" class="form-label">Nội dung</label>
                <textarea
                  v-model="form.message"
                  class="form-control"
                  id="message"
                  rows="5"
                  placeholder="Nhập nội dung tin nhắn"
                  required
                ></textarea>
              </div>

              <div class="d-grid gap-2">
                <button type="submit" class="btn btn-primary btn-lg">
                  <span v-if="!isSubmitting">Gửi tin nhắn</span>
                  <span v-else>
                    <span class="spinner-border spinner-border-sm me-2" role="status" aria-hidden="true"></span>
                    Đang gửi...
                  </span>
                </button>
              </div>
            </form>

            <div v-if="showSuccess" class="alert alert-success mt-3" role="alert">
              ✓ Cảm ơn bạn! Tin nhắn của bạn đã được gửi thành công.
            </div>
            <div v-if="showError" class="alert alert-danger mt-3" role="alert">
              ✗ Có lỗi xảy ra. Vui lòng thử lại.
            </div>
          </div>
        </div>

        <div class="mt-5 text-center">
          <p class="text-muted">Hoặc quay lại <NuxtLink to="/">trang chủ</NuxtLink></p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

definePageMeta({
  title: 'Liên hệ - Nuxt.js Lab 8'
})

const form = ref({
  name: '',
  email: '',
  phone: '',
  subject: '',
  message: ''
})

const isSubmitting = ref(false)
const showSuccess = ref(false)
const showError = ref(false)

const submitForm = async () => {
  isSubmitting.value = true
  showSuccess.value = false
  showError.value = false

  try {
    // Simulate API call
    await new Promise(resolve => setTimeout(resolve, 1500))

    // Success
    showSuccess.value = true
    form.value = {
      name: '',
      email: '',
      phone: '',
      subject: '',
      message: ''
    }

    // Hide success message after 3 seconds
    setTimeout(() => {
      showSuccess.value = false
    }, 3000)
  } catch (error) {
    showError.value = true
  } finally {
    isSubmitting.value = false
  }
}
</script>

<style scoped>
h1 {
  color: #003366;
  font-weight: bold;
  margin-bottom: 40px;
}

.contact-box {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 30px;
  border-radius: 10px;
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.contact-box:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 40px rgba(102, 126, 234, 0.3);
}

.contact-icon {
  font-size: 3rem;
  margin-bottom: 15px;
}

.contact-box h5 {
  font-weight: 600;
  margin-bottom: 10px;
}

.contact-box p {
  margin: 0;
  font-size: 0.95rem;
}

.contact-box a {
  color: white;
  text-decoration: none;
  font-weight: 500;
}

.contact-box a:hover {
  text-decoration: underline;
}

.form-label {
  font-weight: 600;
  color: #333;
  margin-bottom: 8px;
}

.form-control {
  border: 1px solid #ddd;
  border-radius: 5px;
  padding: 10px 12px;
  font-size: 0.95rem;
}

.form-control:focus {
  border-color: #667eea;
  box-shadow: 0 0 0 0.2rem rgba(102, 126, 234, 0.25);
}

textarea.form-control {
  resize: vertical;
  min-height: 120px;
}

.btn-primary {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  border: none;
  font-weight: 600;
  padding: 12px 24px;
  transition: transform 0.2s ease;
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(102, 126, 234, 0.3);
}

.alert {
  border-radius: 8px;
  font-weight: 500;
}

.card {
  border: none;
  border-radius: 10px;
}

.text-muted a {
  color: #667eea;
  text-decoration: none;
  font-weight: 600;
}

.text-muted a:hover {
  text-decoration: underline;
}
</style>

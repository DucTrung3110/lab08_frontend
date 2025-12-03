<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <div class="container">
        <NuxtLink to="/" class="navbar-brand">Nuxt.js</NuxtLink>
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
          </ul>
        </div>
      </div>
    </nav>
    <main class="py-5">
      <NuxtPage />
    </main>
  </div>
</template>

<script setup>
// Bootstrap CSS sẽ được import trong nuxt.config.ts
</script>

<style scoped>
main {
  min-height: calc(100vh - 56px);
}
</style>

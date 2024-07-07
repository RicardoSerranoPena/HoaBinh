<script setup lang="ts">
const runtimeConfig = useRuntimeConfig()
const appConfig = useAppConfig()
</script>

<template>
  <main>
    <div class="hero-desktop" hidden>
      <h1>Sống Đạo Đức</h1>
      <h2 class="subtitle">Không Làm Khổ Mình, Khổ Người, Khổ Chúng Sinh</h2>
    </div>
    <div class="hero-mobile">
      <h1>
        Trung tâm phát triển <br />
        văn hóa đạo đức
      </h1>
    </div>
  </main>
</template>

<style scoped>
h1 {
  text-transform: uppercase;
  font-size: 1.2rem;
  text-align: center;
}
</style>

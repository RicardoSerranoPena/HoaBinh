<template>
  <header class="nav-header">
    <nuxt-link to="/"
      ><img
        class="logo"
        src="~/assets/images/logo.svg"
        width="50"
        height="50"
        alt="Trung tâm phát triển văn hóa đạo đức"
      />
      <h1 class="header-title hidden">Trung tâm phát triển văn hóa đạo đức</h1>
    </nuxt-link>
    <button
      class="mobile-nav-toggle"
      aria-controls="primary-nav-bar"
      aria-expanded="false"
      @click="toggleNavBar"
    >
      <span class="sr-only">Menu</span>
    </button>
    <nav>
      <ul id="primary-nav-bar" data-visible="false" class="primary-nav-bar">
        <li>
          <nuxt-link to="/">Giới Thiệu</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/">Phương Pháp Giáo Dục</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/">Tin Tức</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/">Tuyển Sinh</nuxt-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {
      primaryNav: '',
      navBarToggle: '',
    }
  },
  mounted() {
    this.primaryNav = this.$el.querySelector('.primary-nav-bar')
    this.navBarToggle = this.$el.querySelector('.mobile-nav-toggle')
  },
  methods: {
    toggleNavBar() {
      const visibility = this.primaryNav.getAttribute('data-visible')

      if (visibility === 'false') {
        this.primaryNav.setAttribute('data-visible', true)
        this.navBarToggle.setAttribute('aria-expanded', true)
      } else {
        this.primaryNav.setAttribute('data-visible', false)
        this.navBarToggle.setAttribute('aria-expanded', false)
      }
    },
  },
}
</script>

<style scoped></style>

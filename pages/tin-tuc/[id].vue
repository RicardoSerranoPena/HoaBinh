<template>
  <main>
    <section v-if="!true" class="page">
      <header class="section-title">
        <h1>Tin Tức</h1>
      </header>
      <h2 style="text-align: center">Đang tải...</h2>
    </section>
    <section v-else class="newsletters-page page">
      <header class="section-title">
        <h1>Tin Tức</h1>
      </header>
      <!-- <div class="newsletter-cards" v-if="getObjects.objects">
      <div
        v-for="{ slug, title, metadata } in getObjects.objects"
        :key="title"
        class="card-newsletter"
      >
        <nuxt-link :to="'/tin-tuc/' + slug">
          <div
            class="card-newsletter-hero"
            v-bind:style="{
              backgroundImage: 'url(' + metadata.hero.url + ')',
            }"
          ></div>
          <div class="card-newsletter-body">
            <div class="card-newsletter-title">
              <h2>{{ title }}</h2>
            </div>
            <div class="card-newsletter-description">
              <p>{{ metadata.description }}</p>
            </div>
            <div class="card-newsletter-date">
              <p>{{ metadata.date }}</p>
            </div>
          </div>
        </nuxt-link>
      </div>
    </div> -->
    </section>
  </main>
</template>

<script>
export default {}
</script>

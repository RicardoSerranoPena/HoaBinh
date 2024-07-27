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
      <div class="newsletter-cards">
        <div
          v-for="newsletter in news"
          v-bind:key="newsletter.slug"
          class="card-newsletter"
        >
          <nuxt-link :to="'/tin-tuc/' + newsletter.slug">
            <img
              :src="getImage(newsletter.thumbnail)"
              alt="{{ newsletter.title }}"
            />
            <div class="card-newsletter-body">
              <div class="card-newsletter-title">
                <h2>{{ newsletter.title }}</h2>
              </div>
              <div class="card-newsletter-description">
                <p>{{ newsletter.metadata.mo_ta }}</p>
              </div>
              <div class="card-newsletter-date">
                <p>{{ fixDate(newsletter.published_at) }}</p>
              </div>
            </div>
          </nuxt-link>
        </div>
      </div>
    </section>
  </main>
</template>

<script setup lang="ts">
import { createBucketClient } from '@cosmicjs/sdk'

const cosmic = createBucketClient({
  bucketSlug: 'trung-tam-van-hoa-dao-duc-production',
  readKey: 'ur0XzcVFC0Avd7yIsCq1ScDu7guFza6ZZS7l48rRvfcBqqNRik',
})

const { objects: news } = await cosmic.objects
  .find({ type: 'tin-tucs' })
  .props('slug,title,metadata,published_at,thumbnail')
  .depth(1)

console.log('news: ', news)
console.log('here: ', news.published_at)

function getImage(URL: string) {
  return `${URL}?w=500&auto=format,compression`
}

function fixDate(dateGiven: string) {
  const dateToParse = new Date(dateGiven)
  console.log(dateToParse)
  const options: Intl.DateTimeFormatOptions = {
    weekday: 'long',
    day: 'numeric',
    month: 'short',
    year: 'numeric',
  }
  return dateToParse.toLocaleDateString('vi-VN', options)
}
</script>

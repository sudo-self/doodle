<script setup lang="ts">
import { useSeoMeta, useServerHead } from 'nuxt';

//SEO
useSeoMeta({
  title: 'share your doodles',
  description: 'doodle nuxt is a web application that lets you create, enhance, and share your drawings with the world. Harnessing the power of Cloudflare R2 and Cloudflare AI to store and enhance your drawings.',
  ogTitle: 'doodle',
  ogImage: 'https://pub-c1de1cb456e74d6bbbee111ba9e6c757.r2.dev/icon512.png?theme=light',
  twitterCard: 'summary_large_image',
})

//meta tags
useServerHead({
  meta: [
    { name: 'description', content: 'doodle nuxt dev' },
    { name: 'keywords', content: 'doodle, nuxt, dev, share' },
  ],
})
</script>


<template>
  <AppHeader />
  <UContainer>
    <main class="min-h-[calc(100vh-192px)]">
      <NuxtPage />
    </main>
  </UContainer>
  <AppFooter />
  <UNotifications />
</template>

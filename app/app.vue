<script setup lang="ts">
import { useSeoMeta } from '#app';

//SEO
useSeoMeta({
  title: 'Doodles',
  description: 'Doodle Nuxt is a web application that lets you create, enhance, and share your drawings with the world. Harnessing the power of Cloudflare R2 and Cloudflare AI to store and enhance your drawings.',
  ogTitle: 'Doodle',
  ogImage: 'public/362505213-27d832a8-92e1-43a9-a96b-c0990c0a617d.png',
  twitterCard: 'summary_large_image'
});
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


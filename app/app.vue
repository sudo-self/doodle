<script setup lang="ts">
import { useSeoMeta, useServerHead } from '#app'; // Adjust import based on your Nuxt setup

// Set SEO meta information
useSeoMeta({
  title: 'Share Your Doodles',
  description: 'Doodle Nuxt is a web application that lets you create, enhance, and share your drawings with the world. Harnessing the power of Cloudflare R2 and Cloudflare AI to store and enhance your drawings.',
  ogTitle: 'Doodle',
  ogImage: 'https://pub-c1de1cb456e74d6bbbee111ba9e6c757.r2.dev/icon512.png?theme=light',
  twitterCard: 'summary_large_image'
});

// Set server-side head meta tags
useServerHead({
  meta: [
    { name: 'description', content: 'Doodle Nuxt Dev' },
    { name: 'keywords', content: 'doodle, nuxt, dev, share' }
  ]
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

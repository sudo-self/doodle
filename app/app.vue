<script setup lang="ts">
import { useSeoMeta } from '#app';

//SEO
useSeoMeta({
  title: 'Doodles',
  description: 'Doodle Nuxt is a web application that lets you create, enhance, and share your drawings with the world. Harnessing the power of Cloudflare R2 and Cloudflare AI to store and enhance your drawings.',
  ogTitle: 'Doodle',
  ogDescription: 'Create, enhance, and share your drawings with the world using Doodle Nuxt.',
  ogImage: '/362505213-27d832a8-92e1-43a9-a96b-c0990c0a617d.png',
  ogUrl: 'https://doodle.nuxt.dev',
  ogType: 'website',
  twitterCard: 'summary_large_image',
  twitterSite: '@ilostmyipad',
  twitterCreator: '@ilostmyipad',
  twitterTitle: 'Doodles',
  twitterDescription: 'Doodle Nuxt lets you create, enhance, and share your drawings with the world.',
  twitterImage: '/362505213-27d832a8-92e1-43a9-a96b-c0990c0a617d.png',
  keywords: 'doodles, drawing, art, Cloudflare, Nuxt, web application',
  robots: 'index, follow',
  author: 'jessejesse.com',
  charset: 'utf-8',
  viewport: 'width=device-width, initial-scale=1',
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


<script setup lang="ts">
import { useSeoMeta } from '#app';

// Set SEO meta information
useSeoMeta({
  title: 'Draw and Share Your Art with Atidraw',
  description: 'Atidraw is a web application that lets you create, enhance, and share your drawings with the world. Harnessing the power of Cloudflare R2 and Cloudflare AI to store and enhance your drawings.',
  ogTitle: 'Atidraw',
  ogImage: 'https://assets.hub.nuxt.com/eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1cmwiOiJodHRwczovL2RyYXcubnV4dC5kZXYiLCJpYXQiOjE3MTgwMTc3OTF9.ORrHGOCvTaxN7Lk24swRO7k-mrHmExypBquOA8FUlyg.jpg?theme=light',
  twitterCard: 'summary_large_image',
});
</script>

<template>
  <!-- Your template content goes here -->
</template>


<template>
  <!-- Your template content goes here -->
</template>




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

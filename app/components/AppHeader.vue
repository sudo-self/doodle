<script setup>
const { loggedIn, clear } = useUserSession()
</script>

<template>
  <header class="border-b border-gray-200 dark:border-gray-800 -mb-px sticky top-0 z-50 border-none md:pt-8 md:max-w-2xl mx-auto bg-transparent backdrop-blur-none">
    <UContainer class="flex items-center justify-between gap-3 h-16 bg-gray-400/5 md:rounded-full border-b md:border dark:border-gray-800 bg-gray-50 dark:bg-gray-950">
      <NuxtLink
        to="/"
        class="flex items-center gap-1 flex-shrink-0 font-bold text-xl text-gray-900 dark:text-white flex items-end gap-1.5"   >
      </NuxtLink>
      <a
  href="https://jessejesse.xyz"
  class="flex items-center gap-1 flex-shrink-0 font-bold text-xl text-gray-900 dark:text-white no-underline"
  style="text-decoration: none;"
>
  <img src="https://doodles.jessejesse.com/icon-round-196x196.png" alt="Custom Icon" class="w-8 h-8" />
  <h6 class="flex items-end gap-1.5">
    <span style="color:#34b334;">doodle</span>xyz
  </h6>
</a>
    
      <div class="flex items-center justify-end lg:flex-1 gap-1.5">
        <UButton
          to="https://github.com/sudo-self/doodle/"
          color="gray"
          variant="ghost"
          icon="i-simple-icons-github"
        />
        <UButton
          to="/draw"
          icon="i-ph-pencil"
        >
          Draw
        </UButton>
        <UButton
          v-if="loggedIn"
          color="gray"
          icon="i-ph-power"
          @click="clear"
        />
      </div>
    </UContainer>
  </header>
</template>

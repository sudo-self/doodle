<script setup>
const colorMode = useColorMode()

// Computed
const isDark = computed({
  get() {
    return colorMode.value === 'dark'
  },
  set() {
    colorMode.preference = colorMode.value === 'dark' ? 'light' : 'dark'
  },
})
</script>

<template>
  <footer>
    <UContainer class="py-8 lg:py-4 lg:flex lg:items-center lg:justify-between lg:gap-x-3">
      <div class="lg:flex-1 flex items-center justify-center lg:justify-end gap-x-1.5 lg:order-3">
        <ClientOnly v-if="!colorMode?.forced">
          <UButton
            :icon="isDark ? 'i-heroicons-moon-20-solid' : 'i-heroicons-sun-20-solid'"
            :aria-label="`Switch to ${isDark ? 'light' : 'dark'} mode`"
            color="gray"
            variant="ghost"
            @click="isDark = !isDark"
          />

          <template #fallback>
            <div class="w-8 h-8" />
          </template>
        </ClientOnly>
        <UButton
          to="https://gihub.com/sudo-self"
          color="gray"
          variant="ghost"
          icon="i-simple-icons-github"
        />
        <UButton
          to="https://x.com/ilostmyipad"
          color="gray"
          variant="ghost"
          icon="i-simple-icons-x"
        />
      </div>
      <div class="flex items-center justify-center lg:justify-start lg:flex-1 gap-x-1.5 mt-3 lg:mt-0 lg:order-1">
        <span class="text-sm">
          hosted on&nbsp;
          <UButton
            to="https://cloudflare.com"
            variant="link"
            :padded="false"
            class="text-orange-700"
          >
          Cloudflare Pages&nbsp;by&nbsp;
          </UButton>
          <span class="text-green-700">JesseJesse.com</span>&nbsp;
          <UButton
            to="https://jessejesse.com"
            variant="link"
            :padded="false"
          >
            &nbsp;Nuxt&nbsp;&
          </UButton>
          <UButton
            to="https://hub.nuxt.com/"
            variant="link"
            :padded="false"
          >
            Nuxthub
          </UButton>
        </span>
      </div>
    </UContainer>
  </footer>
</template>


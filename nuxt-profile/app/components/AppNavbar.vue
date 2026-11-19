<script setup lang="ts">
const links = [
  { label: 'Home', to: '/' },
  { label: 'Profile', to: '/profile' },
]
</script>

<template>
  <header class="sticky top-0 z-50 border-b border-brand-200/60 bg-brand-50/80 shadow-[0_8px_24px_-20px_rgba(9,42,50,0.5)] backdrop-blur-xl">
    <nav aria-label="Main navigation" class="mx-auto flex max-w-6xl items-center justify-between px-5 py-4 sm:px-8">
      <NuxtLink
        to="/"
        class="rounded-sm font-display text-xl font-semibold tracking-tight text-brand-800 transition-colors hover:text-accent-700 focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-accent-600"
      >
        WESLEY
      </NuxtLink>
      <ul class="flex items-center gap-5 sm:gap-8">
        <li v-for="link in links" :key="link.to">
          <NuxtLink
            :to="link.to"
            class="relative inline-flex rounded-sm py-1 text-sm font-semibold text-brand-700 transition-colors after:absolute after:-bottom-0.5 after:left-0 after:h-0.5 after:w-full after:origin-left after:scale-x-0 after:bg-accent-500 after:transition-transform after:duration-200 after:content-[''] hover:text-accent-700 hover:after:scale-x-100 focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-accent-600"
            exact-active-class="!text-accent-700 after:scale-x-100"
          >
            {{ link.label }}
          </NuxtLink>
        </li>
      </ul>
    </nav>
  </header>
</template>

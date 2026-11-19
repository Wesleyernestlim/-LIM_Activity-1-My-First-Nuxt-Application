<script setup lang="ts">
defineProps<{ title: string }>()
</script>

<template>
  <section class="group relative overflow-hidden rounded-2xl border-t-2 border-accent-300 bg-white/90 p-6 shadow-[0_18px_48px_-30px_rgba(9,42,50,0.4)] ring-1 ring-brand-200/70 transition duration-300 hover:-translate-y-1 hover:shadow-[0_24px_54px_-28px_rgba(9,42,50,0.38)] sm:p-7">
    <h2 class="mb-5 font-display text-2xl font-semibold tracking-tight text-brand-800">{{ title }}</h2>
    <slot />
  </section>
</template>

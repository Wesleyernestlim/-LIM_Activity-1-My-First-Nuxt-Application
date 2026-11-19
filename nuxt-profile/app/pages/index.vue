<script setup lang="ts">
useHead({ title: 'Home |Wesley' })
</script>

<template>
  <div class="relative isolate">
    <div aria-hidden="true" class="pointer-events-none absolute -left-20 top-0 -z-10 h-64 w-64 rounded-full bg-brand-200/60 blur-3xl sm:-left-28 sm:h-80 sm:w-80" />
    <div aria-hidden="true" class="pointer-events-none absolute -right-16 top-16 -z-10 h-56 w-56 rounded-full bg-accent-200/55 blur-3xl sm:-right-20 sm:h-72 sm:w-72" />

    <div class="flex flex-col items-center gap-8 py-8 text-center md:flex-row md:gap-12 md:py-14 md:text-left">
      <div class="shrink-0 rounded-full bg-gradient-to-br from-brand-400 via-brand-300 to-accent-300 p-1.5 shadow-[0_20px_48px_-20px_rgba(22,67,77,0.55)]">
        <img
          src="/wes.jpg"
          alt="Profile picture"
          class="h-44 w-44 rounded-full border-4 border-brand-50 bg-white object-cover sm:h-52 sm:w-52"
        />
      </div>

      <div class="space-y-5">
        <p class="text-sm font-bold uppercase tracking-[0.18em] text-accent-700">Welcome to my website!</p>
        <h1 class="font-display text-5xl font-semibold leading-[1.05] tracking-tight text-brand-950 sm:text-6xl">
          Hi, I'm Wesley
        </h1>
        <p class="mx-auto max-w-xl text-base leading-7 text-brand-800 md:mx-0">
          Hi! I'm Wesley, a Bachelor of Science in Information Technology student at Caraga State University. 
          I have a passion for web development and enjoy creating beautiful and functional websites. 
          In my free time, I like to explore new technologies, read books, and play video games.
        </p>
        <div class="flex flex-wrap justify-center gap-3 pt-1 md:justify-start">
          <NuxtLink
            to="/profile"
            class="inline-flex items-center rounded-full bg-accent-600 px-6 py-3 text-sm font-bold text-white shadow-[0_10px_24px_-12px_rgba(153,66,47,0.75)] transition duration-200 hover:-translate-y-0.5 hover:bg-accent-700 hover:shadow-[0_14px_28px_-12px_rgba(153,66,47,0.72)] focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-brand-800"
          >
            View My Profile
          </NuxtLink>
        </div>
      </div>
    </div>

    <SectionCard title="Welcome to my humble abode!" class="mt-6">
      <p class="leading-7 text-brand-800">
        Thanks for visiting! Feel free to look around and learn more about me.
      </p>
    </SectionCard>
  </div>
</template>

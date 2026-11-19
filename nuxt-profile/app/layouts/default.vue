<template>
  <div class="flex min-h-screen flex-col overflow-x-hidden bg-brand-50 text-brand-950">
    <AppNavbar />
    <main class="mx-auto w-full max-w-6xl flex-1 px-5 py-10 sm:px-8 sm:py-14">
      <slot />
    </main>
    <footer class="border-t border-brand-200/70 bg-brand-50/80 px-5 py-6 text-center text-sm text-brand-700">
      &copy; {{ new Date().getFullYear() }} Wesley. Built with Nuxt &amp; Tailwind CSS.
    </footer>
  </div>
</template>

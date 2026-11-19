<script setup lang="ts">
useHead({ title: 'Profile | Wesley' })

const info = [
  { label: 'Full Name', value: 'Wesley Ernest Opo Lim' },
  { label: 'Age', value: '20' },
  { label: 'Address', value: 'Butuan City, Agusan del Norte, Philippines' },
  { label: 'Email', value: '@WesleyErnest.lim21@gmail.com' },
  { label: 'Contact No.', value: '+63 962 996 1708' },
]

const education = [
  { level: 'College', school: 'Caraga State University', detail: 'Bachelor of Science in Information Technology', years: '20XX - Present' },
  { level: 'Senior High School', school: 'Ziilovia National High School', detail: 'GAS', years: '2022 - 2024' },
  { level: 'Junior High School', school: 'Ziilovia National High School', detail: '', years: '2018 - 2022' },
  { level: 'Elementary', school: 'Delton View College', detail: '', years: '2010 - 2018' },
]

const skills = ['HTML', 'CSS', 'JavaScript', 'Vue / Nuxt', 'Tailwind CSS', 'Git']
const interests = ['Web Development', 'Technology', 'Design', 'Anime']
const hobbies = ['Reading', 'Gaming', 'Music', 'Bedrotting']
</script>

<template>
  <div class="space-y-6">
    <div class="mb-8">
      <p class="mb-2 text-xs font-bold uppercase tracking-[0.18em] text-accent-700">A little more about me</p>
      <h1 class="font-display text-4xl font-semibold tracking-tight text-brand-950 sm:text-5xl">My Profile</h1>
    </div>

    <SectionCard title="Personal Information">
      <dl class="grid gap-x-8 gap-y-5 sm:grid-cols-2">
        <div v-for="item in info" :key="item.label">
          <dt class="mb-1 text-xs font-bold uppercase tracking-[0.12em] text-brand-600">{{ item.label }}</dt>
          <dd class="break-words font-semibold leading-6 text-brand-950">{{ item.value }}</dd>
        </div>
      </dl>
    </SectionCard>

    <SectionCard title="Educational Background">
      <ul class="ml-1 space-y-0 border-l-2 border-brand-200">
        <li
          v-for="edu in education"
          :key="edu.level"
          class="relative pb-6 pl-6 last:pb-0"
        >
          <span aria-hidden="true" class="absolute -left-[0.47rem] top-1 h-3.5 w-3.5 rounded-full border-[3px] border-white bg-accent-500 ring-2 ring-accent-200" />
          <p class="font-bold text-brand-900">{{ edu.level }}</p>
          <p class="mt-1 leading-6 text-brand-800">{{ edu.school }}<span v-if="edu.detail"> &ndash; {{ edu.detail }}</span></p>
          <p class="mt-1 text-sm font-medium text-brand-600">{{ edu.years }}</p>
        </li>
      </ul>
    </SectionCard>

    <div class="grid gap-6 md:grid-cols-2">
      <SectionCard title="Skills">
        <div class="flex flex-wrap gap-2">
          <span
            v-for="skill in skills"
            :key="skill"
            class="rounded-full border border-brand-200 bg-brand-50 px-3.5 py-1.5 text-sm font-semibold text-brand-800 transition-colors hover:bg-brand-100"
          >
            {{ skill }}
          </span>
        </div>
      </SectionCard>

      <SectionCard title="Interests">
        <div class="flex flex-wrap gap-2">
          <span
            v-for="interest in interests"
            :key="interest"
            class="rounded-full border border-accent-200 bg-accent-50 px-3.5 py-1.5 text-sm font-semibold text-accent-800 transition-colors hover:bg-accent-100"
          >
            {{ interest }}
          </span>
        </div>
      </SectionCard>
    </div>

    <SectionCard title="Hobbies">
      <ul class="flex flex-wrap gap-2">
        <li
          v-for="hobby in hobbies"
          :key="hobby"
          class="rounded-full border border-brand-200 bg-brand-50 px-3.5 py-1.5 text-sm font-semibold text-brand-800 transition-colors hover:border-accent-200 hover:bg-accent-50 hover:text-accent-800"
        >
          {{ hobby }}
        </li>
      </ul>
    </SectionCard>

    <NuxtLink
      to="/"
      class="inline-flex rounded-sm font-semibold text-brand-700 transition-colors hover:text-accent-700 hover:underline focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-accent-600"
    >
      &larr; Back to Home
    </NuxtLink>
  </div>
</template>

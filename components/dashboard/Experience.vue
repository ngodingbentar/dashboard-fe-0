<template>
  <section id="experience" class="mb-16 scroll-mt-16 md:mb-24 lg:mb-36 lg:scroll-mt-24" aria-label="Work experience">
    <div
      class="sticky top-0 z-20 -mx-6 mb-4 w-screen bg-navy/75 px-6 py-5 backdrop-blur md:-mx-12 md:px-12 lg:sr-only lg:relative lg:top-auto lg:mx-auto lg:w-full lg:px-0 lg:py-0 lg:opacity-0">
      <h2 class="text-sm font-bold uppercase tracking-widest text-lightest-slate lg:sr-only">
        Experience
      </h2>
    </div>
    <div>
      <ol class="group/list">
        <ExperienceCard v-for="(job, index) in jobs" :key="index" v-bind="job" />
      </ol>

      <div class="mt-12">
        <a class="inline-flex items-center font-medium leading-tight text-lightest-slate font-semibold text-lightest-slate group"
          aria-label="View Full Resume" href="/resume.pdf" target="_blank" rel="noopener noreferrer">
          <span
            class="border-b border-transparent pb-px transition group-hover:border-green motion-reduce:transition-none">
            Lihat Resume Lengkap
          </span>
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor"
            class="ml-1 inline-block h-4 w-4 shrink-0 -translate-y-px transition-transform group-hover:translate-x-2 group-focus-visible:translate-x-2 motion-reduce:transition-none"
            aria-hidden="true">
            <path fill-rule="evenodd"
              d="M3 10a.75.75 0 01.75-.75h10.638L10.23 5.29a.75.75 0 111.04-1.08l5.5 5.25a.75.75 0 010 1.08l-5.5 5.25a.75.75 0 11-1.04-1.08l4.158-3.96H3.75A.75.75 0 013 10z"
              clip-rule="evenodd"></path>
          </svg>
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
import ExperienceCard from './ExperienceCard.vue';

const jobs = [
  {
    duration: 'Januari 2024 — Sekarang',
    title: 'Frontend Engineer',
    company: 'Setoko',
    companyUrl: 'https://www.linkedin.com/company/setoko/',
    description:
      "Bertanggung jawab penuh dalam pengembangan dan pemeliharaan produk-produk digital utama (website toko online, ERP, CMS) menggunakan stack teknologi modern: Next.Js, React.Js, Typescript, Javascript, Antd, dan Tailwind CSS",
    technologies: ['React', 'Next.js', 'JavaScript', 'TypeScript', 'Antd', 'Tailwind CSS', 'Zustand'],
  },
  {
    duration: 'Agustus 2021 — Agustus 2023',
    title: 'Frontend Engineer',
    company: 'Privy',
    companyUrl: 'https://privy.id/id',
    description:
      'Bertanggung jawab dalam pengembangan dan pemeliharaan produk-produk digital (website tanda tangan digital, CMS, dan layanan surel) menggunakan stack teknologi modern: Nuxt.Js, Vue.Js, Typescript, Javascript, Bootstrap, dan Tailwind CSS.',
    technologies: ['Nuxt.js', 'Vue.js', 'JavaScript', 'TypeScript', 'Bootstrap', 'Tailwind CSS', 'Pinia'],
  },
  {
    duration: 'Oktober 2020 — Maret 2021',
    title: 'Frontend Engineer',
    company: 'Local Tobacco',
    companyUrl: 'https://www.localtobacco.com/',
    description:
      'Bertanggung jawab penuh dalam pengembangan dan pemeliharaan produk-produk digital utama (website Bio-Link, penemuan tempat, CMS,) menggunakan stack teknologi modern: Nuxt.Js, Vue.Js, Typescript, Javascript, dan Tailwind CSS.',
    technologies: ['Nuxt.js', 'Vue.js', 'JavaScript', 'TypeScript', 'Bootstrap', 'Tailwind CSS', 'Pinia'],
  },
];
</script>

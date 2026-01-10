<template>
  <section id="projects" class="mb-16 scroll-mt-16 md:mb-24 lg:mb-36 lg:scroll-mt-24" aria-label="Selected projects">
    <div
      class="sticky top-0 z-20 -mx-6 mb-4 w-screen bg-navy/75 px-6 py-5 backdrop-blur md:-mx-12 md:px-12 lg:sr-only lg:relative lg:top-auto lg:mx-auto lg:w-full lg:px-0 lg:py-0 lg:opacity-0">
      <h2 class="text-sm font-bold uppercase tracking-widest text-lightest-slate lg:sr-only">
        Projects
      </h2>
    </div>
    <div>
      <ul class="group/list">
        <ProjectCard v-for="(project, index) in projects" :key="index" v-bind="project" />
      </ul>

      <div class="mt-12">
        <a class="inline-flex items-center font-medium leading-tight text-lightest-slate font-semibold text-lightest-slate group"
          aria-label="View Full Project Archive" href="/projects">
          <span
            class="border-b border-transparent pb-px transition group-hover:border-green motion-reduce:transition-none">
            Lihat Proyek Lainnya
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
import ProjectCard from './ProjectCard.vue';

const projects = [
  {
    title: 'Hijup',
    url: 'https://hijup.com/',
    description:
      'Proyek e-commerce Hijup adalah pembangunan website dari awal toko online pakaian Islami, di mana saya sebagai Frontend Engineer bertanggung jawab mulai dari penentuan tech stack (Nextjs, Reactjs, Tailwind css, Zustand, Typescript), setup project, implementasi desain UI/UX, integrasi API backend, hingga memastikan performa dan optimasi SEO.',
    technologies: ['React', 'Next.js', 'JavaScript', 'TypeScript', 'Antd', 'Tailwind CSS', 'Zustand'],
    imageUrl: '/img/project/hijup.png',
  },
  {
    title: 'Setoko',
    url: 'https://setoko.co/dew404',
    description:
      'pengembangan website toko online (setoko.co) yang menjual berbagai hal, saya berperan aktif sebagai Frontend Engineer dalam memperbaiki bug teknis, membuat fitur baru, meningkatkan codebase yang sudah ada, dan secara signifikan mengembangkan fitur-fitur baru seperti optimasi checkout dan tampilan produk yang lebih responsif',
    technologies: ['React', 'Next.js', 'JavaScript', 'TypeScript', 'Antd', 'Tailwind CSS', 'Zustand'],
    imageUrl: '/img/project/setoko.png',
  },
  {
    title: 'ERP Setoko',
    url: 'https://web.setoko.co/login',
    description:
      'ERP Setoko adalah platform manajemen bisnis adalah pembangunan website dari awal untuk memudahkan pengelola toko dalam mengelola konten (seperti produk, promo), WMS (Warehouse Management System), CRM (Customer Relationship Management), & POS (Point of Sale)), di mana saya sebagai Frontend Engineer bertanggung jawab penuh mulai dari penentuan tech stack (Nextjs, Reactjs, Tailwind css, Zustand, Typescript), setup project, implementasi desain UI/UX, integrasi API backend, hingga memastikan performa.',
    technologies: ['React', 'Next.js', 'JavaScript', 'TypeScript', 'Antd', 'Tailwind CSS', 'Zustand'],
    imageUrl: '/img/project/web-setoko.png',
  },
  {
    title: 'Privy Corp',
    url: '#',
    description:
      'Bergabung di fase pengembangan lanjutan platform tanda tangan digital yang digunakan oleh perusahaan yang sudah tersertifikasi secara hukum, saya berperan sebagai Frontend Engineer dalam meningkatkan keamanan dan performa alur penandatanganan, memperbaiki bug kritis',
    technologies: ['Vue.js', 'Nuxt.js', 'JavaScript', 'TypeScript', 'Bootstrap', 'Tailwind CSS', 'Pinia'],
    imageUrl: '/img/project/privy-corp.png',
  },
  {
    title: 'Findaya',
    url: '#',
    description:
      'Pembuatan website tanda tangan digital yang digunakan dalam ekosistem Gojek, khususnya untuk produk pinjaman dan paylater seperti GoPay Pinjam dan Modal Toko, di mana saya sebagai Frontend Engineer bertanggung jawab penuh mulai dari penentuan tech stack (Nuxtjs, Vuejs, Tailwind css, Pinia, Typescript), setup project, implementasi desain UI/UX, integrasi API backend, hingga memastikan performa',
    technologies: ['Vue.js', 'Nuxt.js', 'JavaScript', 'TypeScript', 'Bootstrap', 'Tailwind CSS', 'Pinia'],
    imageUrl: '/img/project/findaya.png',
  },
  {
    title: 'Privy Now',
    url: 'http://privynow.com/',
    description:
      'Bergabung di fase pengembangan lanjutan platform tanda tangan digital yang tersertifikasi secara hukum, saya berperan sebagai Frontend Engineer dalam meningkatkan keamanan dan performa alur penandatanganan, memperbaiki bug kritis, dan mengembangkan fitur-fitur verifikasi identitas baru yang kompleks.',
    technologies: ['Vue.js', 'Nuxt.js', 'JavaScript', 'TypeScript', 'Bootstrap', 'Tailwind CSS', 'Pinia'],
    imageUrl: '/img/project/privy-now.jpg',
  },
  {
    title: 'Privy Mail',
    url: '#',
    description:
      'Sebagai Frontend Engineer, saya bertanggung jawab dalam mengembangkan antarmuka pengguna yang intuitif dan responsif untuk sistem email internal perusahaan (mirip Gmail), termasuk fitur manajemen kotak masuk, penyusunan email dengan rich text editor, dan integrasi fungsionalitas pencarian cepat dan aman.',
    technologies: ['Vue.js', 'Nuxt.js', 'JavaScript', 'TypeScript', 'Bootstrap', 'Tailwind CSS', 'Pinia'],
    imageUrl: '/img/project/privy-mail.png',
  },
  {
    title: 'Persona',
    url: 'https://privy-open-source.github.io/design-system',
    description:
      'Sebagai Frontend Engineer, saya bertanggung jawab penuh untuk membangun, mendokumentasikan, dan memelihara Design System agar tim pengembang dapat menciptakan UI yang konsisten, reusable, dan efisien di seluruh produk perusahaan. Design system ini yang akan digunakan untuk semua produk yang ada. Tech stack Nuxtjs, Vuejs, Tailwind css, Typescript.',
    technologies: ['Vue.js', 'Nuxt.js', 'JavaScript', 'TypeScript', 'Bootstrap', 'Tailwind CSS', 'Pinia'],
    imageUrl: '/img/project/persona.png',
  },
  {
    title: 'Dimana',
    url: 'https://www.dimana.io',
    description:
      'Sebagai Frontend Engineer, saya bertanggung jawab untuk membangun antarmuka dan interaksi pengguna pada platform discovery lokasi (dimana.io) yang membantu pengguna menemukan tempat yang sesuai untuk berbagai kebutuhan, meliputi visualisasi peta, implementasi fitur filter canggih, dan memastikan desain yang user-friendly di perangkat mobile. Tech stack Nuxtjs, Vuejs, Tailwind css, Typescript.',
    technologies: ['Vue.js', 'Nuxt.js', 'JavaScript', 'TypeScript', 'Bootstrap', 'Tailwind CSS', 'Pinia'],
    imageUrl: '/img/project/dimana.jpg',
  },
];
</script>

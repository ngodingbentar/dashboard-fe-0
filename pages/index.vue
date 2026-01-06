<template>
  <div class="pointer-events-none fixed inset-0 z-30 transition duration-300"
    :style="`background: radial-gradient(600px at ${mouseX}px ${mouseY}px, rgba(29, 78, 216, 0.15), transparent 80%);`">
  </div>
  <div class="bg-navy min-h-screen text-slate-400 font-sans selection:bg-teal-300 selection:text-teal-900 relative">
    <div class="mx-auto min-h-screen max-w-screen-xl px-6 py-12 font-sans md:px-12 md:py-20 lg:px-24 lg:py-0">
      <div class="lg:flex lg:justify-between lg:gap-4">
        <!-- Sidebar (Left) -->
        <Sidebar class="lg:sticky lg:top-0 lg:flex lg:max-h-screen lg:w-1/2 lg:flex-col lg:justify-between lg:py-24" />

        <!-- Main Content (Right) -->
        <main id="content" class="pt-24 lg:w-1/2 lg:py-24">
          <About />
          <Experience />
          <Projects />
        </main>
      </div>
    </div>
  </div>
</template>

<script setup>
import Sidebar from '~/components/dashboard/Sidebar.vue';
import About from '~/components/dashboard/About.vue';
import Experience from '~/components/dashboard/Experience.vue';
import Projects from '~/components/dashboard/Projects.vue';

const mouseX = ref(0);
const mouseY = ref(0);

function handleMouseMove(event) {
  mouseX.value = event.clientX;
  mouseY.value = event.clientY;
}

onMounted(() => {
  window.addEventListener('mousemove', handleMouseMove);
});

onUnmounted(() => {
  window.removeEventListener('mousemove', handleMouseMove);
});

useHead({
  title: 'Dewa Qintoro | Frontend Engineer',
  meta: [
    { name: 'description', content: 'Dewa Qintoro is a software engineer who builds accessible, pixel-perfect digital experiences for the web.' }
  ],
  bodyAttrs: {
    class: 'bg-navy leading-relaxed text-slate-400 antialiased selection:bg-teal-300 selection:text-teal-900'
  }
})
</script>

<style scoped>
/* Any specific page-level overrides if necessary */
</style>

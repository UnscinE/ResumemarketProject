<script setup lang="ts">
import { useRoute } from 'vue-router'
const route = useRoute()
</script>

<template>
  <nav
    class="sticky top-0 w-full bg-white/70 backdrop-blur-md border-b border-slate-200/80 z-50 transition-all duration-300">
    <div class=" mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
      <div
        class="flex items-center gap-2 font-black text-2xl tracking-tight bg-linear-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent">
        ResumeMarket
      </div>

      <div class="flex flex-row gap-4 justify-between items-center">
        <button @click="$router.push('/candidate/profile')" class="pb-1 font-semibold transition-all duration-350 relative uppercase tracking-wide text-sm
           after:absolute after:bottom-0 after:left-0 after:h-[2px] after:bg-blue-600 after:transition-all after:duration-300
           hover:text-blue-600 active:scale-95" :class="route.path === '/candidate/profile'
            ? 'text-blue-600 after:w-full'
            : 'text-slate-500 after:w-0 hover:after:w-full'">
          Candidate
        </button>

        <div class="h-6 border-l border-slate-300 mx-2"></div>

        <button @click="$router.push('/home')" class="pb-1 font-semibold transition-all duration-350 relative uppercase tracking-wide text-sm
           after:absolute after:bottom-0 after:left-0 after:h-[2px] after:bg-blue-600 after:transition-all after:duration-300
           hover:text-blue-600 active:scale-95" :class="route.path === '/home'
            ? 'text-blue-600 after:w-full'
            : 'text-slate-500 after:w-0 hover:after:w-full'">
          Recruiter
        </button>
      </div>
      <div class="flex items-center gap-4">
        <button
          class="relative p-2 text-slate-500 hover:text-slate-700 rounded-full hover:bg-slate-100 transition cursor-pointer">
          <BellIcon class="w-5 h-5" />
          <span class="absolute top-1.5 right-1.5 w-2 h-2 bg-red-500 rounded-full"></span>
        </button>
        <div class="flex items-center gap-3 border-l border-slate-200 pl-4">
          <div
            class="w-9 h-9 rounded-full bg-slate-200 flex items-center justify-center font-semibold text-sm text-slate-700">
            HR</div>
          <span class="text-sm font-medium text-slate-700 hidden md:inline">Tanawat (Recruiter)</span>
        </div>
      </div>
    </div>
  </nav>

</template>

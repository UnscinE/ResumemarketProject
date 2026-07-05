<script lang="ts">

export default {}
</script>


<template>
  <nav
    class="fixed top-0 w-full bg-white/70 backdrop-blur-md border-b border-slate-200/80 z-50 transition-all duration-300">
    <div class="max-w-7xl mx-auto px-6">
      <div class="flex items-center justify-between h-20">
        <div
          class="flex items-center gap-2 font-black text-2xl tracking-tight bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent">
          ResumeMarket
        </div>

        <div class="hidden md:flex gap-8 font-medium text-slate-600">
          <a href="#features"
            class="transition-colors duration-200 hover:text-blue-600 relative after:absolute after:bottom-[-4px] after:left-0 after:w-0 after:h-[2px] after:bg-blue-600 after:transition-all hover:after:w-full">Features</a>
          <a href="#candidate"
            class="transition-colors duration-200 hover:text-blue-600 relative after:absolute after:bottom-[-4px] after:left-0 after:w-0 after:h-[2px] after:bg-blue-600 after:transition-all hover:after:w-full">Candidates</a>
          <a href="#recruiter"
            class="transition-colors duration-200 hover:text-blue-600 relative after:absolute after:bottom-[-4px] after:left-0 after:w-0 after:h-[2px] after:bg-blue-600 after:transition-all hover:after:w-full">Recruiters</a>
          <a href="/about"
            class="transition-colors duration-200 hover:text-blue-600 relative after:absolute after:bottom-[-4px] after:left-0 after:w-0 after:h-[2px] after:bg-blue-600 after:transition-all hover:after:w-full">About</a>
        </div>

        <div class="flex gap-4 items-center">
          <button class="px-5 py-2.5 font-medium text-slate-600 hover:text-blue-600 transition-colors">
            Login
          </button>
          <button
            class="px-5 py-2.5 bg-slate-900 text-white font-medium rounded-xl hover:bg-slate-800 active:scale-[0.98] transition-all shadow-sm shadow-slate-900/10">
            Sign Up
          </button>
        </div>
      </div>
    </div>
  </nav>
</template>

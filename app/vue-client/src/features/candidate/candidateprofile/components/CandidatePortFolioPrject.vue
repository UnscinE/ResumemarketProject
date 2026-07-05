<script setup lang="ts">
</script>

<template>
  <div class="bg-white rounded-2xl border border-slate-200 shadow-sm p-6">
    <div class="flex justify-between items-center mb-4">
      <h2 class="text-xl font-bold text-slate-900 flex items-center gap-2">
        🚀 ผลงานและโปรเจกต์ (Featured Projects)
      </h2>
      <button class="text-slate-600 hover:bg-slate-100 p-1.5 rounded-lg text-sm font-bold">➕ เพิ่ม</button>
    </div>

    <div class="space-y-4">
      <div
        class="p-4 border border-slate-100 rounded-xl hover:bg-slate-50/80 transition-colors flex flex-col sm:flex-row gap-4 items-start cursor-pointer">
        <div
          class="w-full sm:w-32 h-20 bg-linear-to-br from-indigo-500 to-purple-600 rounded-lg flex items-center justify-center text-white font-black text-xs">
          RM</div>
        <div class="space-y-1">
          <h3 class="font-bold text-base text-slate-900 hover:text-blue-600 transition-colors">Resume Market
            Platform</h3>
          <p class="text-sm text-slate-500 leading-relaxed">แพลตฟอร์มจับคู่ผู้สมัครสาย Tech และ HR
            ด้วยระบบวิดีโอและ AI Parsing พัฒนาด้วย NestJS และ Vue 3</p>
        </div>
      </div>
    </div>
  </div>

</template>

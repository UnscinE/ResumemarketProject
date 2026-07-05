<script setup lang="ts">
</script>

<template>
  <div class="bg-white rounded-2xl border border-slate-200 shadow-sm p-6 relative group">
    <div class="flex justify-between items-center mb-4">
      <h2 class="text-xl font-bold text-slate-900 flex items-center gap-2">
        ℹ️ เกี่ยวกับฉัน (About Me)
      </h2>
      <button class="text-blue-600 hover:bg-blue-50 text-sm font-semibold px-3 py-1.5 rounded-lg transition-colors">
        + อัปโหลดใหม่
      </button>
    </div>

    <div
      class="border-2 min-h-[200px] border-slate-200 hover:border-blue-400 bg-slate-50/50 rounded-xl p-6 transition-colors cursor-pointer flex flex-col items-center justify-center text-center">

      <p class="text-xs text-slate-400">
        Add your summary
      </p>

    </div>
  </div>
</template>

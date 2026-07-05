<script setup lang="ts">
</script>

<template>
  <div class="bg-white rounded-2xl border border-slate-200 shadow-sm p-6">
    <h2 class="text-xl font-bold text-slate-900 flex items-center gap-2 mb-4">
      📹 วิดีโอแนะนำตัว (Video Introduction)
    </h2>

    <div class="grid sm:grid-cols-2 gap-4">
      <div class="space-y-2">
        <span class="text-xs font-bold text-slate-500 uppercase tracking-wider">🇹🇭 เวอร์ชั่นภาษาไทย</span>
        <div
          class="aspect-video bg-slate-900 rounded-xl overflow-hidden shadow-xs relative flex items-center justify-center text-white border border-slate-800">
          <span class="text-sm text-slate-400">Play Thai Video Intro</span>
          <div
            class="absolute bottom-3 left-3 bg-black/60 backdrop-blur-md text-[10px] px-2 py-0.5 rounded text-white font-medium">
            2:15 Min</div>
        </div>
      </div>

      <div class="space-y-2">
        <span class="text-xs font-bold text-slate-500 uppercase tracking-wider">🇬🇧 English Version</span>
        <div
          class="aspect-video bg-slate-900 rounded-xl overflow-hidden shadow-xs relative flex items-center justify-center text-white border border-slate-800">
          <span class="text-sm text-slate-400">Play English Video Intro</span>
          <div
            class="absolute bottom-3 left-3 bg-black/60 backdrop-blur-md text-[10px] px-2 py-0.5 rounded text-white font-medium">
            1:45 Min</div>
        </div>
      </div>
    </div>
  </div>
</template>

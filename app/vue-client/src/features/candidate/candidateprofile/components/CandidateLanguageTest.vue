<script setup lang="ts">
</script>

<template>
  <div class="bg-white rounded-2xl border border-slate-200 shadow-sm p-6">
    <div class="flex justify-between items-center mb-4">
      <h2 class="text-xl font-bold text-slate-900 flex items-center gap-2">
        🗣️ คะแนนทดสอบทางภาษา (Language Scores)
      </h2>
      <button class="text-slate-600 hover:bg-slate-100 p-1.5 rounded-lg text-sm font-bold">➕ เพิ่มคะแนน</button>
    </div>

    <div class="grid sm:grid-cols-2 gap-4">

      <div
        class="p-4 border border-slate-100 rounded-xl bg-slate-50/30 hover:bg-slate-50 transition-colors flex items-center justify-between group">
        <div class="flex items-center gap-4">
          <div
            class="w-14 h-14 bg-linear-to-br from-blue-600 to-indigo-700 rounded-xl flex flex-col items-center justify-center text-white shadow-xs">
            <span class="text-[10px] font-bold tracking-wider opacity-80 uppercase">English</span>
            <span class="font-black text-sm tracking-tight">TOEIC</span>
          </div>
          <div class="space-y-0.5">
            <h3 class="font-bold text-base text-slate-900">TOEIC Listening & Reading</h3>
            <p class="text-xs text-slate-500">สอบเมื่อ: ม.ค. 2026 • Full Score: 990</p>
            <span
              class="inline-flex items-center gap-1 mt-1 text-[11px] font-bold text-emerald-600 bg-emerald-50 px-2 py-0.5 rounded-md border border-emerald-100">
              Advanced (C1)
            </span>
          </div>
        </div>
        <div class="text-right">
          <span class="text-3xl font-black tracking-tight text-blue-600">850</span>
          <p class="text-[10px] font-bold text-slate-400 uppercase tracking-wider">Scores</p>
        </div>
      </div>

      <div
        class="p-4 border border-slate-100 rounded-xl bg-slate-50/30 hover:bg-slate-50 transition-colors flex items-center justify-between group">
        <div class="flex items-center gap-4">
          <div
            class="w-14 h-14 bg-linear-to-br from-red-500 to-rose-600 rounded-xl flex flex-col items-center justify-center text-white shadow-xs">
            <span class="text-[10px] font-bold tracking-wider opacity-80 uppercase">English</span>
            <span class="font-black text-sm tracking-tight">IELTS</span>
          </div>
          <div class="space-y-0.5">
            <h3 class="font-bold text-base text-slate-900">IELTS Academic</h3>
            <p class="text-xs text-slate-500">สอบเมื่อ: มี.ค. 2026 • Full Score: 9.0</p>
            <span
              class="inline-flex items-center gap-1 mt-1 text-[11px] font-bold text-emerald-600 bg-emerald-50 px-2 py-0.5 rounded-md border border-emerald-100">
              Good User (B2)
            </span>
          </div>
        </div>
        <div class="text-right">
          <span class="text-3xl font-black tracking-tight text-rose-600">6.5</span>
          <p class="text-[10px] font-bold text-slate-400 uppercase tracking-wider">Band</p>
        </div>
      </div>

    </div>
  </div>
</template>

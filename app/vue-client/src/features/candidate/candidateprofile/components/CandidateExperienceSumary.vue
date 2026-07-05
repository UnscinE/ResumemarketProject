<script setup lang="ts"></script>


<template>
  <div class="border border-slate-200 rounded-2xl p-6 bg-white shadow-sm">
    <p class="text-base font-bold text-slate-900 tracking-tight flex items-center gap-2">
      💼 ประวัติการทำงาน (Experience Path)
    </p>

    <div class="space-y-4 mt-6">
      <div class="relative border-l-2 border-slate-100 pl-5 space-y-6 ml-2">

        <div class="relative group cursor-pointer">
          <span
            class="absolute -left-[26px] top-1 w-2.5 h-2.5 bg-blue-600 rounded-full border-2 border-white ring-4 ring-blue-50 group-hover:scale-110 transition-transform"></span>

          <div class="flex flex-col space-y-0.5">
            <div class="flex items-center gap-2">
              <h3 class="text-sm font-bold text-slate-900 group-hover:text-blue-600 transition-colors">
                Programmer (Full-time)
              </h3>
              <span
                class="text-[9px] font-bold text-emerald-600 bg-emerald-50 border border-emerald-100 px-1.5 py-0.5 rounded-md">
                Present
              </span>
            </div>
            <p class="text-xs font-semibold text-slate-700">Woxa Group</p>
            <p class="text-[11px] text-slate-400 mt-0.5">ม.ค. 2025 - ปัจจุบัน · 1 ปี 6 เดือน</p>
          </div>
        </div>

        <div class="relative group cursor-pointer">
          <span
            class="absolute -left-[26px] top-1 w-2.5 h-2.5 bg-slate-300 rounded-full border-2 border-white ring-4 ring-slate-50 group-hover:scale-110 transition-transform"></span>

          <div class="flex flex-col space-y-0.5">
            <h3 class="text-sm font-bold text-slate-900 group-hover:text-blue-600 transition-colors">
              Programmer (Internship)
            </h3>
            <p class="text-xs font-semibold text-slate-600">มหาวิทยาลัยขอนแก่น</p>
            <p class="text-[11px] text-slate-400 mt-0.5">มิ.ย. 2024 - ธ.ค. 2024 · 6 เดือน</p>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

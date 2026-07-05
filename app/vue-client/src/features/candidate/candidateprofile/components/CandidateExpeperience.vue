<script setup lang="ts">
</script>

<template>
  <div class="bg-white rounded-2xl border border-slate-200 shadow-sm p-6">
    <div class="flex justify-between items-center mb-6">
      <h2 class="text-xl font-bold text-slate-900 flex items-center gap-2">
        💼 ประวัติการทำงาน (Experience)
      </h2>
      <button class="text-slate-600 hover:bg-slate-100 p-1.5 rounded-lg text-sm font-bold transition-colors">
        ➕ เพิ่มประสบการณ์
      </button>
    </div>

    <div class="space-y-6">

      <div class="flex gap-4 items-start relative group">
        <div class="w-12 h-12 bg-slate-900 text-white font-black text-xs rounded-xl flex items-center justify-center shrink-0 shadow-xs">
          WOXA
        </div>

        <div class="space-y-1.5 flex-1">
          <div class="flex flex-wrap items-center justify-between gap-x-2">
            <h3 class="text-base font-bold text-slate-900 hover:text-blue-600 cursor-pointer transition-colors">
              Full Stack Developer
            </h3>
            <span class="text-xs font-bold text-emerald-600 bg-emerald-50 border border-emerald-100 px-2 py-0.5 rounded-md">
              งานปัจจุบัน
            </span>
          </div>

          <p class="text-sm font-semibold text-slate-700">Woxa Group · งานประจำ (Full-time)</p>
          <p class="text-xs text-slate-400">ม.ค. 2025 - ปัจจุบัน · 1 ปี 6 เดือน</p>
          <p class="text-xs text-slate-500 font-medium">ขอนแก่น, ประเทศไทย · แบบผสม (Hybrid)</p>

          <ul class="list-disc list-inside text-xs text-slate-600 space-y-1 pt-1.5 leading-relaxed pl-1">
            <li>ออกแบบและพัฒนาฟีเจอร์ต่างๆ บนระบบ Resume Market Platform โดยใช้ Vue 3 และ NestJS</li>
            <li>ดูแลระบบฐานข้อมูล PostgreSQL และจัดการ API Endpoint ให้มีความเสถียรและปลอดภัย</li>
            <li>ทำงานร่วมกับทีมด้วยระบบ Agile methodology และควบคุมเวอร์ชันโค้ดผ่าน Git</li>
          </ul>
        </div>
      </div>

      <hr class="border-slate-100" />

      <div class="flex gap-4 items-start relative group">
        <div class="w-12 h-12 bg-blue-600 text-white font-black text-xs rounded-xl flex items-center justify-center shrink-0 shadow-xs">
          TR
        </div>

        <div class="space-y-1.5 flex-1">
          <h3 class="text-base font-bold text-slate-900 hover:text-blue-600 cursor-pointer transition-colors">
            Frontend Developer Intern
          </h3>
          <p class="text-sm font-semibold text-slate-700">Talad Resume · ฝึกงาน (Internship)</p>
          <p class="text-xs text-slate-400">มิ.ย. 2024 - ธ.ค. 2024 · 6 เดือน</p>
          <p class="text-xs text-slate-500 font-medium">กรุงเทพมหานคร, ประเทศไทย · ทำงานทางไกล (Remote)</p>

          <ul class="list-disc list-inside text-xs text-slate-600 space-y-1 pt-1.5 leading-relaxed pl-1">
            <li>พัฒนา UI คอมโพเนนต์หน้าเว็บให้รองรับการแสดงผลทุกหน้าจอ (Responsive Web Design) ด้วย Tailwind CSS</li>
            <li>ทำโปรแกรมเชื่อมต่อข้อมูลกับ RESTful API และจัดการ State ภายในแอปพลิเคชัน</li>
            <li>ปรับปรุงประสิทธิภาพความเร็วในการโหลดหน้าเว็บ (Web Performance Optimization)</li>
          </ul>
        </div>
      </div>

    </div>
  </div>
</template>

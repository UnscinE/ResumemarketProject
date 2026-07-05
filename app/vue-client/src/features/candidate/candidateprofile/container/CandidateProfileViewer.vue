<script setup lang="ts">
import HomePageNav from '@/components/homepage/HomePageNav.vue';
import ChatBox from '@/features/chat/container/ChatBox.vue';
import CoreSkillsSection from '../components/CandidateCoreSkill.vue';
import EducationSection from '../components/CandidateEducation.vue';
import WorkExperienceSection from '../components/CandidateExpeperience.vue';
import EpereienceSumary from '../components/CandidateExperienceSumary.vue';
import LanguageTest from '../components/CandidateLanguageTest.vue';
import PortFolioPrject from '../components/CandidatePortFolioPrject.vue';
import ResumeSection from '../components/CandidateResumeSection.vue';
import SummarySection from '../components/CandidateSummarySection.vue';
import VideosSection from '../components/CandidateVideosSection.vue';

</script>

<template>
  <div id="homepage" class="min-h-screen bg-slate-100 text-slate-900 font-sans antialiased">
    <HomePageNav />

    <div class="max-w-6xl mx-auto px-4 mt-6 ">

      <div class="bg-white rounded-2xl border border-slate-200 shadow-sm overflow-hidden pb-8">

        <div id="coverphoto" class="relative h-48 sm:h-64 bg-linear-to-r from-sky-400 to-blue-600 overflow-hidden">
          <div
            class="absolute inset-0 opacity-20 bg-[radial-gradient(circle_at_center,rgba(255,255,255,0.2)_0,transparent_100%)]">
          </div>
        </div>

        <div class="flex flex-row justify-between">
          <div class="px-8 relative">

            <div class="relative inline-block">
              <div
                class="w-32 h-32 sm:w-40 sm:h-40 rounded-full bg-slate-300 border-4 border-white shadow-sm overflow-hidden -mt-16 sm:-mt-20 relative z-10">
                <div class="w-full h-full flex items-center justify-center bg-slate-900 text-white font-bold text-xl">
                  รูปโปรไฟล์
                </div>
              </div>
            </div>

            <div class="grid md:grid-cols-12 gap-6 mt-4">

              <div class="md:col-span-8 space-y-2">
                <div class="flex items-center gap-2">
                  <h1 class="text-2xl sm:text-3xl font-bold text-slate-900 tracking-tight">Tanawat Tanatka</h1>
                  <div>✅</div>
                  <span class="text-sm rounded-md text-slate-500 font-medium">He/Him</span>
                </div>
                <p class="text-xl font-black">Job title</p>
                <p class="text-lg text-slate-600 font-normal">Co-founder at Talad Resume</p>
                <p class="text-lg text-blue-500 font-normal underline">Expected salary : 15000</p>

                <div class="flex flex-wrap gap-x-3 gap-y-1 text-sm text-slate-500 font-medium">
                  <span>ขอนแก่น, ขอนแก่น, ประเทศไทย</span>
                  <span class="text-blue-600 hover:underline cursor-pointer">ข้อมูลติดต่อ</span>
                </div>
              </div>

            </div>

            <div class="mt-6 bg-blue-50/60 border border-blue-100 rounded-2xl p-4 max-w-xl relative group">
              <button
                class="absolute top-4 right-4 text-slate-400 hover:text-slate-600 opacity-0 group-hover:opacity-100 transition-opacity">✏️</button>
              <h3 class="text-sm font-bold text-slate-900">เปิดรับโอกาสงาน</h3>
              <p class="text-xs text-slate-600 mt-1">ขอนแก่น อีก 3 รายการ | ในสถานที่ · แบบผสม</p>
              <span
                class="text-xs font-bold text-blue-600 hover:underline cursor-pointer mt-2 inline-block">แสดงรายละเอียด</span>
            </div>

          </div>

          <div class="container max-w-md p-4">
            <EpereienceSumary />
          </div>
        </div>
      </div>

      <div class="grid md:grid-cols-12 gap-4 mt-4 pb-24">

        <div class="md:col-span-8 space-y-4">
          <SummarySection />
          <ResumeSection />
          <VideosSection />
          <PortFolioPrject />
          <LanguageTest />

        </div>

        <div class="md:col-span-4 space-y-4">
          <CoreSkillsSection />
          <WorkExperienceSection />
          <EducationSection />

        </div>

      </div>

      <ChatBox />

    </div>
  </div>
</template>

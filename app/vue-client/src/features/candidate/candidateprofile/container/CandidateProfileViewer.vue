<script setup lang="ts">
import { ref } from 'vue';
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

// นำเข้าไอคอนสำหรับส่วนด้านขวาเพิ่มเติม (เช่น Plus เพื่อให้เพิ่มฝั่งขวาได้)
import { CirclePlus, ChevronDown, GripVertical, Trash2, Plus } from '@lucide/vue';

/* ==========================================================================
   [ระบบฝั่งซ้าย (Left Side)]
   ========================================================================== */
const componentMapLeft: Record<string, any> = {
  summary: SummarySection,
  resume: ResumeSection,
  videos: VideosSection,
  portfolio: PortFolioPrject,
  language: LanguageTest
};

const availableSectionsLeft = [
  { id: 'summary', name: 'บทสรุป (Summary)' },
  { id: 'resume', name: 'เรซูเม่ (Resume)' },
  { id: 'videos', name: 'วิดีโอแนะนำตัว (Videos)' },
  { id: 'portfolio', name: 'ผลงาน (Portfolio Project)' },
  { id: 'language', name: 'ผลทดสอบภาษา (Language Test)' }
];

const activeSectionsLeft = ref<string[]>([]);
const isLeftMenuOpen = ref(false);

const addSectionLeft = (typeId: string) => {
  if (!activeSectionsLeft.value.includes(typeId)) {
    activeSectionsLeft.value.push(typeId);
  }
  isLeftMenuOpen.value = false;
};

const removeSectionLeft = (typeId: string) => {
  activeSectionsLeft.value = activeSectionsLeft.value.filter(id => id !== typeId);
};


/* ==========================================================================
   [ระบบฝั่งขวา (Right Side)] - เพิ่มระบบจัดการเข้ามาใหม่
   ========================================================================== */
const componentMapRight: Record<string, any> = {
  coreSkills: CoreSkillsSection,
  workExperience: WorkExperienceSection,
  education: EducationSection
};

const availableSectionsRight = [
  { id: 'coreSkills', name: 'ทักษะหลัก (Core Skills)' },
  { id: 'workExperience', name: 'ประสบการณ์ทำงาน (Work Experience)' },
  { id: 'education', name: 'ประวัติการศึกษา (Education)' }
];

// ตั้งค่าเริ่มต้นให้ฝั่งขวามี 3 Section นี้อยู่แล้วตามดีไซน์เดิมของคุณครับ
const activeSectionsRight = ref<string[]>(['coreSkills', 'workExperience', 'education']);
const isRightMenuOpen = ref(false);

const addSectionRight = (typeId: string) => {
  if (!activeSectionsRight.value.includes(typeId)) {
    activeSectionsRight.value.push(typeId);
  }
  isRightMenuOpen.value = false;
};

const removeSectionRight = (typeId: string) => {
  activeSectionsRight.value = activeSectionsRight.value.filter(id => id !== typeId);
};


/* ==========================================================================
   [ระบบลากสลับลำดับด้วย HTML5 API] - แยกกลุ่มฝั่งซ้ายและฝั่งขวาชัดเจน
   ========================================================================== */
const draggedLeftIndex = ref<number | null>(null);
const draggedRightIndex = ref<number | null>(null);

// จัดการฝั่งซ้าย
const onLeftDragStart = (index: number) => { draggedLeftIndex.value = index; };
const onLeftDragEnd = () => { draggedLeftIndex.value = null; };
const onLeftDragOver = (index: number) => {
  if (draggedLeftIndex.value === null || draggedLeftIndex.value === index) return;
  const items = [...activeSectionsLeft.value];
  const draggedItem = items[draggedLeftIndex.value];
  items.splice(draggedLeftIndex.value, 1);
  items.splice(index, 0, draggedItem);
  activeSectionsLeft.value = items;
  draggedLeftIndex.value = index;
};

// จัดการฝั่งขวา
const onRightDragStart = (index: number) => { draggedRightIndex.value = index; };
const onRightDragEnd = () => { draggedRightIndex.value = null; };
const onRightDragOver = (index: number) => {
  if (draggedRightIndex.value === null || draggedRightIndex.value === index) return;
  const items = [...activeSectionsRight.value];
  const draggedItem = items[draggedRightIndex.value];
  items.splice(draggedRightIndex.value, 1);
  items.splice(index, 0, draggedItem);
  activeSectionsRight.value = items;
  draggedRightIndex.value = index;
};
</script>

<template>
  <div id="homepage" class="min-h-screen bg-slate-100 text-slate-900 font-sans antialiased">
    <HomePageNav />

    <div class="max-w-6xl mx-auto px-4 mt-6">

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
                  รูปโปรไฟล์</div>
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
          <div v-for="(sectionId, index) in activeSectionsLeft" :key="sectionId" draggable="true"
            @dragstart="onLeftDragStart(index)" @dragover.prevent="onLeftDragOver(index)" @dragend="onLeftDragEnd"
            class="relative group/section bg-white border border-slate-200 rounded-2xl transition-all duration-200"
            :class="{ 'opacity-40 scale-[0.99] border-blue-400 border-dashed': draggedLeftIndex === index }">
            <div
              class="absolute right-4 top-4 z-40 opacity-0 group-hover/section:opacity-100 transition-opacity flex items-center gap-2 bg-white/95 shadow-sm p-1.5 rounded-lg border border-slate-200">
              <div
                class="cursor-grab active:cursor-grabbing p-1 hover:bg-slate-100 rounded text-slate-400 hover:text-slate-600">
                <GripVertical class="w-4 h-4" />
              </div>
              <button @click="removeSectionLeft(sectionId)"
                class="p-1 hover:bg-rose-50 text-slate-400 hover:text-rose-600 rounded transition-colors cursor-pointer">
                <Trash2 class="w-4 h-4" />
              </button>
            </div>
            <div class="p-2">
              <component :is="componentMapLeft[sectionId]" />
            </div>
          </div>

          <div class="relative">
            <button @click="isLeftMenuOpen = !isLeftMenuOpen"
              class="flex w-full bg-slate-200 border-2 border-dashed border-slate-300 rounded-lg h-40 items-center justify-center gap-2 text-slate-600 hover:bg-slate-300/70 transition-colors cursor-pointer">
              <span>เพิ่มข้อมูลฝั่งซ้าย (Add Section)</span>
              <CirclePlus class="w-5 h-5" />
              <ChevronDown class="w-4 h-4" />
            </button>

            <div v-if="isLeftMenuOpen"
              class="absolute left-0 right-0 mt-2 bg-white border border-slate-200 rounded-xl shadow-lg z-50 overflow-hidden">
              <div class="p-2 max-h-60 overflow-y-auto">
                <button v-for="item in availableSectionsLeft" :key="item.id" @click="addSectionLeft(item.id)"
                  :disabled="activeSectionsLeft.includes(item.id)"
                  class="w-full text-left px-4 py-3 text-sm rounded-lg hover:bg-slate-50 flex justify-between items-center disabled:opacity-50 disabled:bg-slate-100 disabled:cursor-not-allowed">
                  <span class="font-medium text-slate-700">{{ item.name }}</span>
                  <span v-if="activeSectionsLeft.includes(item.id)"
                    class="text-xs text-emerald-600 bg-emerald-50 px-2 py-0.5 rounded-md">เพิ่มอยู่แล้ว</span>
                  <span v-else class="text-xs text-blue-600">+ เพิ่ม</span>
                </button>
              </div>
            </div>
          </div>
        </div>

        <div class="md:col-span-4 space-y-4">
          <div v-for="(sectionId, index) in activeSectionsRight" :key="sectionId" draggable="true"
            @dragstart="onRightDragStart(index)" @dragover.prevent="onRightDragOver(index)" @dragend="onRightDragEnd"
            class="relative group/section bg-white border border-slate-200 rounded-2xl transition-all duration-200"
            :class="{ 'opacity-40 scale-[0.99] border-blue-400 border-dashed': draggedRightIndex === index }">
            <div
              class="absolute right-4 top-4 z-40 opacity-0 group-hover/section:opacity-100 transition-opacity flex items-center gap-2 bg-white/95 shadow-sm p-1.5 rounded-lg border border-slate-200">
              <div
                class="cursor-grab active:cursor-grabbing p-1 hover:bg-slate-100 rounded text-slate-400 hover:text-slate-600">
                <GripVertical class="w-4 h-4" />
              </div>
              <button @click="removeSectionRight(sectionId)"
                class="p-1 hover:bg-rose-50 text-slate-400 hover:text-rose-600 rounded transition-colors cursor-pointer"
                title="ลบส่วนนี้">
                <Trash2 class="w-4 h-4" />
              </button>
            </div>

            <div class="p-2">
              <component :is="componentMapRight[sectionId]" />
            </div>
          </div>

          <div class="relative">
            <button @click="isRightMenuOpen = !isRightMenuOpen"
              class="flex w-full bg-slate-200/60 border-2 border-dashed border-slate-300 rounded-lg py-4 items-center justify-center gap-2 text-slate-500 hover:bg-slate-200 transition-colors text-sm cursor-pointer">
              <Plus class="w-4 h-4" />
              <span>จัดการข้อมูลฝั่งขวา</span>
            </button>

            <div v-if="isRightMenuOpen"
              class="absolute left-0 right-0 mt-2 bg-white border border-slate-200 rounded-xl shadow-lg z-50 overflow-hidden">
              <div class="p-2 max-h-60 overflow-y-auto">
                <button v-for="item in availableSectionsRight" :key="item.id" @click="addSectionRight(item.id)"
                  :disabled="activeSectionsRight.includes(item.id)"
                  class="w-full text-left px-4 py-3 text-sm rounded-lg hover:bg-slate-50 flex justify-between items-center disabled:opacity-50 disabled:bg-slate-100 disabled:cursor-not-allowed">
                  <span class="font-medium text-slate-700">{{ item.name }}</span>
                  <span v-if="activeSectionsRight.includes(item.id)"
                    class="text-xs text-emerald-600 bg-emerald-50 px-2 py-0.5 rounded-md">เพิ่มอยู่แล้ว</span>
                  <span v-else class="text-xs text-blue-600">+ เพิ่มคอลัมน์นี้</span>
                </button>
              </div>
            </div>
          </div>

        </div>

      </div>

      <ChatBox />

    </div>
  </div>
</template>

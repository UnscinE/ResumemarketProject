<script setup lang="ts">
import { ref, reactive, computed } from 'vue'
// นำเข้าไอคอนจาก Lucide Vue
import {
  Bell as BellIcon,
  SlidersHorizontal as SlidersHorizontalIcon,
  Search as SearchIcon,
  Heart as HeartIcon,
  GraduationCap as GraduationCapIcon,
  Wallet as WalletIcon,
  Briefcase as BriefcaseIcon
} from 'lucide-vue-next'

// State สำหรับการค้นหาและคัดกรอง (Filters)
const searchQuery = ref('')
const sortBy = ref('relevant')

const filters = reactive({
  selectedField: '',
  experience: [] as string[],
  minSalary: null,
  maxSalary: null,
  school: ''
})

// Mock Data แคนดิเดต (อิงตามข้อมูลแบบย่อยใน Padlet ของคุณ)
const candidates = ref([
  {
    id: 1,
    name: 'John Doe',
    initials: 'JD',
    role: 'Full-Stack Developer',
    field: 'Tech / Developer',
    experienceType: 'First Jobber',
    expText: 'First Jobber (6 Months Internship)',
    education: 'Computer Engineering, KMUTT',
    salary: 40000,
    skills: ['React', 'Node.js', 'TypeScript'],
    bgColor: 'bg-blue-100',
    textColor: 'text-blue-600',
    isFavorite: false
  },
  {
    id: 2,
    name: 'Somsri S.',
    initials: 'SS',
    role: 'UI/UX Designer',
    field: 'UI/UX Designer',
    experienceType: 'First Jobber',
    expText: 'First Jobber (Freelance Portfolio)',
    education: 'Digital Media, Chulalongkorn University',
    salary: 30000,
    skills: ['Figma', 'Wireframing', 'Design System'],
    bgColor: 'bg-purple-100',
    textColor: 'text-purple-600',
    isFavorite: true
  }
])

// Logic ในการกรองข้อมูล (Computed Filter)
const filteredCandidates = computed(() => {
  return candidates.value.filter(candidate => {
    // 1. กรองจากแถบค้นหา (Search Query)
    const matchesSearch = candidate.name.toLowerCase().includes(searchQuery.value.toLowerCase()) ||
      candidate.role.toLowerCase().includes(searchQuery.value.toLowerCase()) ||
      candidate.skills.some(s => s.toLowerCase().includes(searchQuery.value.toLowerCase()))

    // 2. กรองตามสายงาน (Field)
    const matchesField = !filters.selectedField || candidate.field === filters.selectedField

    // 3. กรองตามประสบการณ์ (Experience Checkbox)
    const matchesExp = filters.experience.length === 0 || filters.experience.includes(candidate.experienceType)

    // 4. กรองตามฐานเงินเดือน (Salary Range)
    const matchesMinSalary = !filters.minSalary || candidate.salary >= filters.minSalary
    const matchesMaxSalary = !filters.maxSalary || candidate.salary <= filters.maxSalary

    // 5. กรองตามสถาบัน (Education)
    const matchesSchool = !filters.school || candidate.education.toLowerCase().includes(filters.school.toLowerCase())

    return matchesSearch && matchesField && matchesExp && matchesMinSalary && matchesMaxSalary && matchesSchool
  })
})

//ฟังก์ชันการทำงานต่างๆ (Methods)
const toggleFavorite = (candidate: { isFavorite: boolean }) => {
  candidate.isFavorite = !candidate.isFavorite
}

const clearFilters = () => {
  filters.selectedField = ''
  filters.experience = []
  filters.minSalary = null
  filters.maxSalary = null
  filters.school = ''
  searchQuery.value = ''
}

const previewProfile = (id: any) => {
  alert(`Opening Pre-view Profile Modal for candidate ID: ${id}`)
}

const contactCandidate = (id: any) => {
  alert(`Connecting HR with candidate ID: ${id}`)
}

</script>


<template>
  <div id="homepage" class="min-h-screen bg-slate-50 text-slate-900 font-sans">

    <nav class="bg-white border-b border-slate-200 sticky top-0 z-50">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
        <div class="flex items-center gap-2">
          <div
            class="w-8 h-8 rounded-lg bg-gradient-to-r from-blue-600 to-indigo-600 flex items-center justify-center text-white font-bold text-lg">
            T</div>
          <span class="font-bold text-xl tracking-tight text-slate-900">Talent<span
              class="text-blue-600">Hub</span></span>
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

    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8">

      <div class="mb-8">
        <h1 class="text-3xl font-extrabold text-slate-900 tracking-tight">Discover Talents</h1>
        <p class="text-slate-500 mt-1">Find and filter the perfect candidates for your company openings.</p>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-4 gap-8 items-start">

        <aside class="bg-white p-6 rounded-2xl border border-slate-200 shadow-sm lg:sticky lg:top-24">
          <div class="flex items-center justify-between mb-6">
            <h2 class="font-bold text-lg text-slate-900 flex items-center gap-2">
              <SlidersHorizontalIcon class="w-5 h-5 text-blue-600" /> Filters
            </h2>
            <button @click="clearFilters"
              class="text-xs font-semibold text-blue-600 hover:text-indigo-600 transition cursor-pointer">Clear
              all</button>
          </div>

          <div class="space-y-6">
            <div>
              <label class="block text-xs font-bold text-slate-500 uppercase tracking-wider mb-2">Candidate
                Field</label>
              <select v-model="filters.selectedField"
                class="w-full bg-slate-50 border border-slate-200 rounded-xl px-3 py-2.5 text-sm font-medium text-slate-700 focus:outline-none focus:border-blue-500 focus:ring-2 focus:ring-blue-100 transition">
                <option value="">All Fields</option>
                <option value="Tech / Developer">Tech / Developer</option>
                <option value="UI/UX Designer">UI/UX Designer</option>
                <option value="Marketing / Content">Marketing / Content</option>
              </select>
            </div>

            <div>
              <label class="block text-xs font-bold text-slate-500 uppercase tracking-wider mb-2">Experience
                Level</label>
              <div class="space-y-2 text-sm font-medium text-slate-600">
                <label class="flex items-center gap-2.5 cursor-pointer">
                  <input type="checkbox" value="First Jobber" v-model="filters.experience"
                    class="w-4 h-4 rounded border-slate-300 text-blue-600 focus:ring-blue-500" /> First Jobber
                </label>
                <label class="flex items-center gap-2.5 cursor-pointer">
                  <input type="checkbox" value="Junior" v-model="filters.experience"
                    class="w-4 h-4 rounded border-slate-300 text-blue-600 focus:ring-blue-500" /> Junior (1-3 years)
                </label>
                <label class="flex items-center gap-2.5 cursor-pointer">
                  <input type="checkbox" value="Senior" v-model="filters.experience"
                    class="w-4 h-4 rounded border-slate-300 text-blue-600 focus:ring-blue-500" /> Senior (5+ years)
                </label>
              </div>
            </div>

            <div>
              <label class="block text-xs font-bold text-slate-500 uppercase tracking-wider mb-2">Expected Salary
                (THB)</label>
              <div class="grid grid-cols-2 gap-2">
                <input type="number" v-model="filters.minSalary" placeholder="Min"
                  class="w-full bg-slate-50 border border-slate-200 rounded-xl px-3 py-2 text-sm focus:outline-none focus:border-blue-500" />
                <input type="number" v-model="filters.maxSalary" placeholder="Max"
                  class="w-full bg-slate-50 border border-slate-200 rounded-xl px-3 py-2 text-sm focus:outline-none focus:border-blue-500" />
              </div>
            </div>

            <div>
              <label class="block text-xs font-bold text-slate-500 uppercase tracking-wider mb-2">Education /
                School</label>
              <input type="text" v-model="filters.school" placeholder="e.g. KMUTT"
                class="w-full bg-slate-50 border border-slate-200 rounded-xl px-3 py-2.5 text-sm focus:outline-none focus:border-blue-500" />
            </div>
          </div>
        </aside>

        <main class="lg:col-span-3 space-y-6">

          <div class="bg-white p-4 rounded-2xl border border-slate-200 shadow-sm flex flex-col md:flex-row gap-3">
            <div class="relative flex-1">
              <SearchIcon class="w-5 h-5 text-slate-400 absolute left-3.5 top-1/2 -translate-y-1/2" />
              <input type="text" v-model="searchQuery" placeholder="Search by skills, keywords, or talent name..."
                class="w-full bg-slate-50 border border-slate-200 rounded-xl pl-11 pr-4 py-3 text-sm focus:outline-none focus:border-blue-500 focus:ring-2 focus:ring-blue-100 transition" />
            </div>
            <button
              class="bg-gradient-to-r from-blue-600 to-indigo-600 hover:from-blue-700 hover:to-indigo-700 text-white font-semibold text-sm px-6 py-3 rounded-xl shadow-sm transition cursor-pointer">
              Search Talent
            </button>
          </div>

          <div class="flex items-center justify-between text-sm text-slate-500 font-medium px-1">
            <span>Showing <strong class="text-slate-800">{{ filteredCandidates.length }}</strong> qualified
              talents</span>
            <div class="flex items-center gap-1.5">
              <span>Sort by:</span>
              <select v-model="sortBy"
                class="bg-transparent border-0 font-bold text-slate-800 focus:ring-0 p-0 cursor-pointer text-sm outline-none">
                <option value="relevant">Most Relevant</option>
                <option value="newest">Newest Profiles</option>
              </select>
            </div>
          </div>

          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">

            <div v-for="candidate in filteredCandidates" :key="candidate.id"
              class="bg-white border border-slate-200 rounded-2xl p-6 shadow-sm hover:border-blue-300 hover:shadow-md transition flex flex-col justify-between group">
              <div>
                <div class="flex items-start justify-between mb-4">
                  <div class="flex gap-3.5 items-center">
                    <div
                      :class="`w-14 h-14 rounded-full ${candidate.bgColor} font-bold ${candidate.textColor} flex items-center justify-center text-lg shadow-inner`">
                      {{ candidate.initials }}
                    </div>
                    <div>
                      <h3 class="font-bold text-slate-900 group-hover:text-blue-600 transition">{{ candidate.name }}
                      </h3>
                      <p class="text-sm font-semibold text-indigo-600">{{ candidate.role }}</p>
                    </div>
                  </div>
                  <button @click="toggleFavorite(candidate)" class="p-2 rounded-xl transition cursor-pointer"
                    :class="candidate.isFavorite ? 'text-red-500 bg-red-50' : 'text-slate-400 hover:text-red-500 hover:bg-red-50'">
                    <HeartIcon class="w-5 h-5" :class="{ 'fill-current': candidate.isFavorite }" />
                  </button>
                </div>

                <div class="space-y-2.5 my-4">
                  <div class="flex items-center gap-2 text-xs font-medium text-slate-500">
                    <GraduationCapIcon class="w-4 h-4 text-slate-400" />
                    <span>{{ candidate.education }}</span>
                  </div>
                  <div class="flex items-center gap-2 text-xs font-medium text-slate-500">
                    <WalletIcon class="w-4 h-4 text-slate-400" />
                    <span>{{ candidate.salary.toLocaleString() }} THB / Month</span>
                  </div>
                  <div class="flex items-center gap-2 text-xs font-medium text-slate-500">
                    <BriefcaseIcon class="w-4 h-4 text-slate-400" />
                    <span>{{ candidate.expText }}</span>
                  </div>
                </div>

                <div class="flex flex-wrap gap-1.5 mt-4">
                  <span v-for="skill in candidate.skills" :key="skill"
                    class="px-2.5 py-1 bg-slate-100 rounded-md text-xs font-semibold text-slate-600">
                    {{ skill }}
                  </span>
                </div>
              </div>

              <div class="mt-6 pt-4 border-t border-slate-100 flex gap-2">
                <button @click="previewProfile(candidate.id)"
                  class="flex-1 bg-slate-50 hover:bg-slate-100 text-slate-700 font-bold text-xs py-2.5 px-4 rounded-xl transition cursor-pointer">
                  Pre-view Profile
                </button>
                <button @click="contactCandidate(candidate.id)"
                  class="flex-1 bg-blue-600 hover:bg-blue-700 text-white font-bold text-xs py-2.5 px-4 rounded-xl shadow-sm transition cursor-pointer">
                  Contact Now
                </button>
              </div>
            </div>

          </div>

          <div v-if="filteredCandidates.length === 0"
            class="text-center py-12 bg-white rounded-2xl border border-slate-200">
            <p class="text-slate-500 font-medium">No candidates match your current filters.</p>
          </div>

        </main>
      </div>
    </div>
  </div>
</template>

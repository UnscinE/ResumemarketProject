<script setup lang="ts">
</script>

<template>
  <div
    class="flex flex-col items-center min-h-screen bg-slate-50/50 text-slate-800 antialiased selection:bg-blue-500 selection:text-white">
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
            <a href="#about"
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

    <section
      class="relative w-full pt-40 pb-28 bg-gradient-to-br from-blue-50 via-indigo-50/30 to-white overflow-hidden">
      <div class="absolute top-20 right-0 w-96 h-96 bg-blue-400/10 rounded-full blur-3xl -z-10"></div>
      <div class="absolute bottom-0 left-10 w-80 h-80 bg-indigo-400/10 rounded-full blur-3xl -z-10"></div>

      <div class="max-w-7xl mx-auto px-6">
        <div class="grid lg:grid-cols-12 gap-16 items-center">
          <div class="lg:col-span-7 text-left">
            <span
              class="inline-flex items-center gap-1.5 bg-blue-50 border border-blue-100 text-blue-700 px-4 py-2 rounded-full text-xs font-semibold tracking-wide uppercase">
              <span class="w-1.5 h-1.5 rounded-full bg-blue-600 animate-pulse"></span>
              Professional Profile Platform
            </span>

            <h1 class="text-5xl lg:text-7xl font-extrabold mt-6 leading-[1.1] tracking-tight text-slate-900">
              Discover Talent <br />
              <span class="bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent">
                Beyond a Resume
              </span>
            </h1>

            <p class="mt-6 text-xl text-slate-500/90 leading-relaxed font-normal max-w-xl">
              สร้างโปรไฟล์มืออาชีพ แสดงผลงาน ประสบการณ์ และตัวตนของคุณให้โดดเด่นและเข้าตา HR มากกว่าแค่กระดาษ Resume
              แผ่นเดิมๆ
            </p>

            <div class="flex flex-wrap gap-4 mt-10">
              <button
                class="px-8 py-4 bg-blue-600 text-white rounded-xl font-semibold shadow-lg shadow-blue-600/20 hover:bg-blue-700 active:scale-[0.98] transition-all">
                Create Profile
              </button>
              <button
                class="px-8 py-4 border border-slate-200 bg-white hover:bg-slate-50 text-slate-700 rounded-xl font-semibold active:scale-[0.98] transition-all">
                Explore Talent
              </button>
            </div>
          </div>

          <div class="lg:col-span-5 w-full">
            <div
              class="bg-white rounded-3xl border border-slate-100 shadow-2xl shadow-indigo-100/80 p-8 transform hover:-translate-y-1 transition-transform duration-300">
              <div class="flex items-center gap-5">
                <div class="relative">
                  <div
                    class="w-20 h-20 rounded-2xl bg-gradient-to-tr from-blue-500 to-indigo-600 shadow-md shadow-blue-500/20 flex items-center justify-center text-white text-2xl font-bold">
                    TT
                  </div>
                  <span
                    class="absolute bottom-0 right-0 w-4 h-4 bg-green-500 border-4 border-white rounded-full"></span>
                </div>

                <div>
                  <h3 class="font-bold text-2xl text-slate-900 tracking-tight">
                    Tanawat Tanatka
                  </h3>
                  <p class="text-blue-600 font-medium text-sm mt-0.5">
                    Full Stack Developer
                  </p>
                </div>
              </div>

              <div class="mt-8">
                <h4 class="font-bold text-xs text-slate-400 uppercase tracking-wider">
                  Core Skills
                </h4>
                <div class="flex flex-wrap gap-2 mt-3">
                  <span
                    class="px-3 py-1.5 bg-slate-50 text-slate-600 border border-slate-200/60 rounded-lg text-xs font-semibold hover:bg-blue-50 hover:text-blue-600 hover:border-blue-100 transition-colors">Vue</span>
                  <span
                    class="px-3 py-1.5 bg-slate-50 text-slate-600 border border-slate-200/60 rounded-lg text-xs font-semibold hover:bg-blue-50 hover:text-blue-600 hover:border-blue-100 transition-colors">Angular</span>
                  <span
                    class="px-3 py-1.5 bg-slate-50 text-slate-600 border border-slate-200/60 rounded-lg text-xs font-semibold hover:bg-blue-50 hover:text-blue-600 hover:border-blue-100 transition-colors">Node.js</span>
                  <span
                    class="px-3 py-1.5 bg-slate-50 text-slate-600 border border-slate-200/60 rounded-lg text-xs font-semibold hover:bg-blue-50 hover:text-blue-600 hover:border-blue-100 transition-colors">Go</span>
                  <span
                    class="px-3 py-1.5 bg-slate-50 text-slate-600 border border-slate-200/60 rounded-lg text-xs font-semibold hover:bg-blue-50 hover:text-blue-600 hover:border-blue-100 transition-colors">Docker</span>
                </div>
              </div>

              <div class="mt-8">
                <h4 class="font-bold text-xs text-slate-400 uppercase tracking-wider">
                  Featured Projects
                </h4>
                <div class="space-y-3 mt-3">
                  <div
                    class="flex items-center justify-between border border-slate-100 bg-slate-50/50 rounded-xl p-4 hover:bg-slate-50 transition-colors cursor-pointer group">
                    <span class="font-medium text-sm text-slate-700 group-hover:text-blue-600 transition-colors">Resume
                      Market Platform</span>
                    <span class="text-xs text-slate-400 group-hover:translate-x-1 transition-transform">→</span>
                  </div>

                  <div
                    class="flex items-center justify-between border border-slate-100 bg-slate-50/50 rounded-xl p-4 hover:bg-slate-50 transition-colors cursor-pointer group">
                    <span class="font-medium text-sm text-slate-700 group-hover:text-blue-600 transition-colors">Smart
                      Shoe AI Project</span>
                    <span class="text-xs text-slate-400 group-hover:translate-x-1 transition-transform">→</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="features" class="py-28 w-full bg-white">
      <div class="max-w-7xl mx-auto px-6">
        <div class="text-center max-w-2xl mx-auto">
          <h2 class="text-4xl font-extrabold text-slate-900 tracking-tight">
            Platform Features
          </h2>
          <p class="text-slate-500 mt-4 text-lg">
            Everything you need to showcase your professional profile and attract premium global recruiters.
          </p>
        </div>

        <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-8 mt-20">
          <div
            class="group border border-slate-100 bg-slate-50/40 rounded-2xl p-8 hover:bg-white hover:shadow-xl hover:shadow-slate-100 hover:border-blue-100 transition-all duration-300">
            <div
              class="w-12 h-12 bg-blue-100 text-blue-600 rounded-xl flex items-center justify-center font-bold text-xl group-hover:bg-blue-600 group-hover:text-white transition-colors">
              📄</div>
            <h3 class="font-bold text-xl text-slate-900 mt-6">Resume Upload</h3>
            <p class="text-slate-500 text-sm mt-2 leading-relaxed">Upload and parse your PDF Resume effortlessly in
              seconds.</p>
          </div>
          <div
            class="group border border-slate-100 bg-slate-50/40 rounded-2xl p-8 hover:bg-white hover:shadow-xl hover:shadow-slate-100 hover:border-blue-100 transition-all duration-300">
            <div
              class="w-12 h-12 bg-indigo-100 text-indigo-600 rounded-xl flex items-center justify-center font-bold text-xl group-hover:bg-indigo-600 group-hover:text-white transition-colors">
              💼</div>
            <h3 class="font-bold text-xl text-slate-900 mt-6">Portfolio</h3>
            <p class="text-slate-500 text-sm mt-2 leading-relaxed">Showcase your best production-ready projects
              beautifully.</p>
          </div>
          <div
            class="group border border-slate-100 bg-slate-50/40 rounded-2xl p-8 hover:bg-white hover:shadow-xl hover:shadow-slate-100 hover:border-blue-100 transition-all duration-300">
            <div
              class="w-12 h-12 bg-purple-100 text-purple-600 rounded-xl flex items-center justify-center font-bold text-xl group-hover:bg-purple-600 group-hover:text-white transition-colors">
              📹</div>
            <h3 class="font-bold text-xl text-slate-900 mt-6">Video Intro</h3>
            <p class="text-slate-500 text-sm mt-2 leading-relaxed">Introduce yourself directly and let your soft skills
              shine.</p>
          </div>
          <div
            class="group border border-slate-100 bg-slate-50/40 rounded-2xl p-8 hover:bg-white hover:shadow-xl hover:shadow-slate-100 hover:border-blue-100 transition-all duration-300">
            <div
              class="w-12 h-12 bg-teal-100 text-teal-600 rounded-xl flex items-center justify-center font-bold text-xl group-hover:bg-teal-600 group-hover:text-white transition-colors">
              ⏳</div>
            <h3 class="font-bold text-xl text-slate-900 mt-6">Timeline</h3>
            <p class="text-slate-500 text-sm mt-2 leading-relaxed">Share your career journey and personal milestones.
            </p>
          </div>
        </div>
      </div>
    </section>

    <section id="candidate" class="py-28 w-full bg-slate-50/70 border-y border-slate-100">
      <div class="max-w-7xl mx-auto px-6">
        <div class="grid lg:grid-cols-2 gap-16 items-center">
          <div>
            <h2 class="text-4xl font-extrabold text-slate-900 tracking-tight">
              For Candidates
            </h2>
            <p class="mt-4 text-lg text-slate-500 leading-relaxed">
              สร้างความต่างให้โปรไฟล์ของคุณ โดดเด่นกว่าการส่งแค่กระดาษประวัติแบบเดิมๆ เพื่อดึงดูดบริษัท Tech
              ชั้นนำทั่วโลก
            </p>

            <ul class="grid grid-cols-1 sm:grid-cols-2 gap-4 mt-8 font-medium text-slate-600">
              <li class="flex items-center gap-3"><span class="text-green-500">✓</span> Professional Profile</li>
              <li class="flex items-center gap-3"><span class="text-green-500">✓</span> Resume PDF Upload</li>
              <li class="flex items-center gap-3"><span class="text-green-500">✓</span> Video Introduction</li>
              <li class="flex items-center gap-3"><span class="text-green-500">✓</span> Portfolio Projects</li>
              <li class="flex items-center gap-3"><span class="text-green-500">✓</span> Skills Verification</li>
            </ul>
          </div>

          <div
            class="bg-white p-4 aspect-video rounded-2xl border-2 border-slate-100 shadow-xl shadow-slate-200/50 flex items-center justify-center min-h-7.5 text-slate-400 font-medium border-dashed">
            <iframe class="w-full h-full" src="https://www.youtube.com/embed/8sphSCBpQ_M" frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
              referrerpolicy="strict-origin-when-cross-origin" allowfullscreen>
            </iframe>
          </div>
        </div>
      </div>
    </section>

    <section id="recruiter" class="py-28 w-full bg-white">
      <div class="max-w-7xl mx-auto px-6">
        <div class="grid lg:grid-cols-2 gap-16 items-center">
          <div
            class="bg-slate-50 p-8 rounded-2xl border border-slate-100 flex items-center justify-center min-h-[250px] text-slate-400 font-medium order-last lg:order-first border-dashed border-2">
            [ Search Dashboard UI Mockup ]
          </div>

          <div>
            <h2 class="text-4xl font-extrabold text-slate-900 tracking-tight">
              For Recruiters
            </h2>
            <p class="mt-4 text-lg text-slate-500 leading-relaxed">
              ประหยัดเวลาการสรรหา ค้นหาผู้สมัครคุณภาพสูงได้ตรงจุด จากคลังทักษะ ผลงานชิ้นเอก และคลิปวิดีโอแนะนำตัวจริง
            </p>

            <ul class="grid grid-cols-1 sm:grid-cols-2 gap-4 mt-8 font-medium text-slate-600">
              <li class="flex items-center gap-3"><span class="text-blue-600">✦</span> Smart Skill Search</li>
              <li class="flex items-center gap-3"><span class="text-blue-600">✦</span> Advanced Filters</li>
              <li class="flex items-center gap-3"><span class="text-blue-600">✦</span> Candidate Favorites</li>
              <li class="flex items-center gap-3"><span class="text-blue-600">✦</span> Portfolio Deep Review</li>
              <li class="flex items-center gap-3"><span class="text-blue-600">✦</span> Direct Instant Contact</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section
      class="w-full py-24 bg-gradient-to-r from-slate-900 via-indigo-950 to-slate-900 text-white relative overflow-hidden">
      <div class="absolute inset-0 bg-[radial-gradient(circle_at_top_right,rgba(59,130,246,0.15),transparent_50%)]">
      </div>
      <div class="max-w-4xl mx-auto text-center px-6 relative z-10">
        <h2 class="text-4xl lg:text-5xl font-black tracking-tight leading-tight">
          Ready to Build Your <br class="hidden sm:inline" /> Professional Presence?
        </h2>
        <p class="mt-6 text-xl text-indigo-200/80 font-normal">
          เริ่มสร้างสรรค์ตัวตนในโลกดิจิทัลของคุณได้ฟรีตั้งแต่วันนี้
        </p>
        <button
          class="mt-8 px-8 py-4 bg-blue-600 hover:bg-blue-500 text-white rounded-xl font-bold transition-all shadow-xl shadow-blue-600/30 active:scale-[0.98]">
          Get Started For Free
        </button>
      </div>
    </section>

    <footer class="w-full bg-slate-950 text-slate-400 py-16 border-t border-slate-900">
      <div class="max-w-7xl mx-auto px-6 flex flex-col md:flex-row justify-between items-center gap-6">
        <div class="text-center md:text-left">
          <h3 class="text-2xl font-black text-white tracking-tight">
            ResumeMarket
          </h3>
          <p class="text-slate-500 mt-2 text-sm">
            Professional Profile & Resume Discovery Platform
          </p>
        </div>
        <div class="text-sm text-slate-600">
          &copy; 2026 ResumeMarket. All rights reserved.
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
// นี่เป็นส่วน script ของ Vue แบบ "script setup" (Composition API แบบย่อ)
// นำเข้าไอคอนลูกศรจากไลบรารี heroicons เพื่อใช้เป็นคอมโพเนนต์ในปุ่ม
import { ArrowRightIcon } from '@heroicons/vue/24/solid'
</script>

<template>
<section class="relative w-full min-h-screen flex items-center overflow-hidden">

  <div class="w-full max-w-6xl mx-auto px-6 lg:px-8">
    <div class="grid lg:grid-cols-2 gap-14 items-center">

      <!-- LEFT SIDE -->
      <!-- ฝั่งซ้าย: ข้อความแนะนำตัว ปุ่ม CTA และการ์ดสถิติ -->
        <div class="flex flex-col justify-center">

  <!-- Title -->
  <!-- ส่วนหัวหลัก: ชื่อ/ตำแหน่ง และเอฟเฟกต์ไล่สีบนข้อความ -->
  <div class="text-white" data-aos="fade-right">
          <h1 class="font-bold text-4xl md:text-5xl lg:text-6xl leading-tight">
            Hi, I'm
            <span class="text-transparent bg-clip-text bg-gradient-to-r from-pink-300 to-rose-300">
              I-NET 👋🏻
            </span>
          </h1>

          <p class="font-medium text-lg md:text-xl mt-4">
            Full-Stack Developer & UX/UI Designer
          </p>
        </div>

  <!-- Description -->
  <!-- ย่อหน้าอธิบายสั้น ๆ (ตัวอย่างข้อความ placeholder) -->
  <p class="text-white pt-2 max-w-xl text-lg leading-relaxed">
          Lorem ipsum dolor sit amet consectetur adipisicing 
          elit amet consectetur adipisicing elit.
        </p>

  <!-- Buttons -->
  <!-- ปุ่ม: Contact และ Download CV (มีเอฟเฟกต์ hover และ animation เล็กน้อย) -->
  <div
          class="flex flex-col sm:flex-row gap-4 pt-8"
          data-aos="fade-up"
          data-aos-delay="300"
        >
          <!-- Contact -->
          <!-- ปุ่มติดต่อ: ใช้ gradient เป็นพื้นหลัง และไอคอนลูกศรขวา -->
          <button
            class="group px-8 py-4 rounded-xl font-semibold
            flex items-center justify-center
            text-white
            bg-gradient-to-r from-pink-300 to-rose-400
            transition-all duration-300
            hover:scale-105 hover:shadow-lg hover:shadow-pink-300/40"
          >
            Contact Me
            <ArrowRightIcon
              class="w-5 h-5 ml-2 transition-transform group-hover:translate-x-1"
            />
          </button>

          <!-- Download -->
          <!-- ลิงก์ดาวน์โหลด: ใช้ attribute download เพื่อดาวน์โหลดไฟล์จาก public -->
          <a
            href="/Rinthida Saracheep.png"
            download
            class="group px-8 py-4 rounded-xl font-semibold
            flex items-center justify-center gap-3
            border-2 border-white/60
            bg-white/10 hover:bg-white/20
            text-white backdrop-blur-sm
            transition-all duration-300 hover:scale-105"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="w-6 h-6 transition-transform group-hover:translate-y-1"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M12 4v10m0 0l-4-4m4 4l4-4m-9 6h10" />
            </svg>
            Download CV
          </a>
        </div>

  <!-- Stats Cards -->
  <!-- การ์ดสถิติ: แสดงตัวเลขสั้น ๆ เช่น จำนวนโปรเจกต์, ปีประสบการณ์ ฯลฯ -->
  <div 
          class="flex flex-wrap items-center justify-center lg:justify-start gap-6 pt-12"
          data-aos="fade-up"
          data-aos-delay="400"
        >

          <!-- Card 1 -->
          <!-- การ์ด: Projects (ตัวเลขหลักและคำอธิบาย) -->
          <div class="bg-white/40 backdrop-blur-md
            border border-white/50
            px-8 py-6 rounded-2xl shadow-md
            transition-all duration-300
            hover:shadow-xl hover:scale-105
            text-center min-w-[140px]">

            <div class="text-3xl font-bold
              text-transparent bg-clip-text
              bg-gradient-to-r from-pink-400 to-rose-500">
              20+
            </div>
            <div class="text-gray-500 text-sm mt-2 tracking-wide">
              Projects
            </div>
          </div>


          <!-- Card 2 -->
          <!-- การ์ด: Years (ประสบการณ์เป็นปี) -->
          <div class="bg-white/40 backdrop-blur-md
            border border-white/50
            px-8 py-6 rounded-2xl shadow-md
            transition-all duration-300
            hover:shadow-xl hover:scale-105
            text-center min-w-[140px]">

            <div class="text-3xl font-bold
              text-transparent bg-clip-text
              bg-gradient-to-r from-rose-400 to-pink-500">
              1.5+
            </div>
            <div class="text-gray-500 text-sm mt-2 tracking-wide">
              Years
            </div>
          </div>

          <!-- Card 3 -->
          <!-- การ์ด: End-to-End Development (ความเชี่ยวชาญ) -->
          <div class="bg-white/40 backdrop-blur-md
            border border-white/50
            px-8 py-6 rounded-2xl shadow-md
            transition-all duration-300
            hover:shadow-xl hover:scale-105
            text-center min-w-[160px]">

            <div class="text-3xl font-bold
              text-transparent bg-clip-text
              bg-gradient-to-r from-purple-400 to-pink-400">
              End-to-End
            </div>
            <div class="text-gray-500 text-sm mt-2 tracking-wide">
              Development
            </div>
          </div>

        </div>

      </div>

  <!-- RIGHT SIDE -->
  <!-- ฝั่งขวา: ภาพโปรไฟล์/ภาพประกอบ พร้อมพื้นหลัง gradient และเอฟเฟกต์เรืองแสง -->
  <div class="flex justify-center lg:justify-end relative">

        <div
          class="relative
          bg-gradient-to-br from-rose-100 via-pink-100 to-purple-100
          shadow-xl
          rounded-[50%_40%_30%_60%/60%_30%_70%_30%]
          p-8 border border-white/50"
          data-aos="zoom-in"
        >

          <!-- glowing circle -->
          <!-- วงกลมเรืองแสงเป็นองค์ประกอบตกแต่ง (absolute, blur, pulse) -->
          <div class="absolute -top-4 -right-6 w-20 h-20
            bg-gradient-to-br from-pink-300 to-rose-400
            rounded-full blur-2xl opacity-70 animate-pulse">
          </div>

          <img
            src="/Subject 3.png"
            alt="I-NET"
            class="w-[600px] h-[400px] object-contain relative z-10"
          />

        </div>

      </div>

    </div>
  </div>

</section>
</template>




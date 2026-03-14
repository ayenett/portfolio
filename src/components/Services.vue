<template>
  <section class="relative py-24 overflow-hidden" id="services">

    <!-- Container -->
    <div class="relative z-10 max-w-7xl mx-auto px-6 lg:px-8">

      <!-- Title -->
      <div class="text-center mb-20" data-aos="fade-up">
        <h2 class="text-4xl md:text-5xl font-bold text-white mb-6">
          My
          <span
            class="text-transparent bg-clip-text bg-gradient-to-r from-pink-300 to-rose-300">
            Services
          </span>
        </h2>

        <p
          class="text-white text-lg max-w-3xl mx-auto"
          data-aos="fade-up"
          data-aos-delay="100"
        >
          Lorem ipsum dolor sit amet consectetur adipisicing elit.
          Atque, ullam provident, rerum est blanditiis minus ullam provident,
          rerum est blanditiis minus.
        </p>
      </div>

      <!-- Grid Cards -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">

        <div
          v-for="(service, index) in services"
          :key="service.id"
          data-aos="fade-up"
          :data-aos-delay="(index * 100) + 200"
          class="group relative p-8 rounded-3xl
          bg-white/60
          backdrop-blur-xl
          border border-white/70
          shadow-xl shadow-gray-300/40
          transition-all duration-500
          hover:-translate-y-3
          hover:shadow-2xl
          hover:bg-white/80"
        >

          <!-- Background Gradient Layer -->
          <div
            class="absolute inset-0 bg-gradient-to-br
            from-rose-50 via-pink-50 to-gray-100
            rounded-3xl">
          </div>

          <!-- Icon -->
          <div class="relative z-10">
            <div
              class="inline-flex items-center justify-center
              w-16 h-16 rounded-xl
              bg-gradient-to-br from-rose-200 via-pink-100 to-gray-100
              border border-gray-300/50
              group-hover:scale-110
              transition-transform duration-300"
            >
              <component
                :is="service.icon"
                class="w-8 h-8 text-gray-500"
              />
            </div>
          </div>

          <!-- Text -->
          <div class="relative z-10 mt-6">
            <h3 class="text-xl font-semibold text-gray-700">
              {{ service.name }}
            </h3>

            <p class="text-gray-500 leading-relaxed mt-3">
              {{ service.description }}
            </p>
          </div>

          <!-- Arrow Icon -->
          <div
            class="absolute bottom-6 right-6 opacity-0
            group-hover:opacity-100
            transform translate-x-4
            group-hover:translate-x-0
            transition-all duration-300"
          >
            <ArrowRightIcon class="w-6 h-6 text-gray-500" />
          </div>

        </div>

      </div>

      <!-- Bottom Button -->
      <div
        class="text-center mt-20"
        data-aos="fade-up"
        data-aos-delay="800"
      >
        <div class="inline-flex flex-col sm:flex-row gap-4 items-center">

          <button
            class="group px-8 py-4 rounded-xl border
            border-2 border-white
            text-gray-500
            font-semibold
            shadow-lg backdrop-blur-md
            transition-all duration-300
            hover:bg-white hover:shadow-xl
            flex items-center gap-3"
          >
            Get In Touch

            <ChatBubbleLeftRightIcon
              class="w-6 h-6 text-gray-500
              transition-transform duration-300
              group-hover:translate-x-1"
            />
          </button>

        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
import {
  ChatBubbleLeftRightIcon,
  ArrowRightIcon
} from '@heroicons/vue/24/outline'

import {
  CodeBracketIcon,
  DevicePhoneMobileIcon,
  DocumentTextIcon,
  EnvelopeIcon,
  PaintBrushIcon,
  ComputerDesktopIcon
} from '@heroicons/vue/24/solid'

import { ref } from 'vue'

const services = ref([
  {
    id: 1,
    icon: CodeBracketIcon,
    name: "Web Development",
    description:
      "Lorem ipsum dolor sit amet dolor sit amet sit amet dolor sit amet."
  },
  {
    id: 2,
    icon: DocumentTextIcon,
    name: "Technical Writing",
    description:
      "Lorem ipsum dolor sit amet dolor sit amet sit amet dolor sit amet."
  },
  {
    id: 3,
    icon: DevicePhoneMobileIcon,
    name: "Mobile Development",
    description:
      "Lorem ipsum dolor sit amet dolor sit amet sit amet dolor sit amet."
  },
  {
    id: 4,
    icon: EnvelopeIcon,
    name: "Email Marketing",
    description:
      "Lorem ipsum dolor sit amet dolor sit amet sit amet dolor sit amet."
  },
  {
    id: 5,
    icon: PaintBrushIcon,
    name: "UX/UI Design",
    description:
      "Lorem ipsum dolor sit amet dolor sit amet sit amet dolor sit amet."
  },
  {
    id: 6,
    icon: ComputerDesktopIcon,
    name: "Web Design",
    description:
      "Lorem ipsum dolor sit amet dolor sit amet sit amet dolor sit amet."
  }
])
</script>

<style>
</style>

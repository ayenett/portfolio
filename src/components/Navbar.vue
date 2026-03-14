<template>
  <header class="flex justify-between items-center p-6 bg-opacity-50 relative z-20">
    <div class="text-3xl font-bold text-white drop-shadow-lg">
  Portfolio
</div>
    <div class="md:hidden z-30">
        <button type="button"
        class="block focus:outline-none p-2 rounded-lg bg-pink-800/500  
        hover:bg-pink-600 transition-all duration-300"
        @click="isMenuOpen = !isMenuOpen">

<div class="relative w-9 h-9 flex items-center justify-center">

  <!-- เส้นบน -->
  <span :class="[
    'absolute w-6 h-0.5 rounded-full bg-white transition-all duration-300',
    isMenuOpen ? 'rotate-45' : '-translate-y-2'
  ]"></span>

  <!-- เส้นกลาง -->
  <span :class="[
    'absolute w-6 h-0.5 rounded-full bg-white transition-all duration-300',
    isMenuOpen ? 'opacity-0' : ''
  ]"></span>

  <!-- เส้นล่าง -->
  <span :class="[
    'absolute w-6 h-0.5 rounded-full bg-white transition-all duration-300',
    isMenuOpen ? '-rotate-45' : 'translate-y-2'
  ]"></span>
</div>
        </button>
    </div>
    <nav
      :class="[
        'fixed inset-0 z-20 flex flex-col items-center justify-center bg-gray-100 md:relative md:bg-transparent md:flex md:justify-between md:flex-row',
        isMenuOpen ? 'block' : 'hidden'
      ]">
    <ul class="flex flex-col items-center space-y-5 md:flex-row md:space-x-5 md:space-y-0">
    <li v-for="item in Menu" :key="item.name" class="group relative">
        <a href="item.href"
        class="relative block text-pink-300 hover:text-pink-500 
        transition-all duration-300 text-xl  md:text-base font-medium group" 
        @click="scrollToSection(item.href)">
        {{ item.name }}
        <span class="absolute  bottom-0 left-0  w-0 h-0.5 bg-pink-500  transition-all duration-300 group-hover:w-full"></span>
        </a>
    </li>
    </ul>
    <div class="mt-8 md:mt-0 md:ml-8">
  <button 
  class="px-6 py-2.5 
  bg-gradient-to-r from-pink-300 to-rose-300
  text-white font-semibold tracking-wide
  drop-shadow-[0_1px_2px_rgba(0,0,0,0.15)]
  rounded-full
  transition-all duration-300
  hover:shadow-lg hover:shadow-pink-300/40
  hover:scale-105 active:scale-95"
>
  Let's Talk
</button>


    </div>
    </nav>

  </header>
</template>

<script setup>
import { ref } from 'vue';

const Menu = ref([
    {name: 'Services', href: '#services'},
    {name: 'About Me', href: '#about'},
    {name: 'Skills', href: '#skills'},
    {name: 'Experience & Activities', href: '#experience'},
    {name: 'Contact', href: '#contact'},
]);
const isMenuOpen = ref(false);
const scrollToSection = (href) => {
   isMenuOpen.value = false;
   const section = document.querySelector(href);
   if (section) {
       section.scrollIntoView({ behavior: 'smooth' });
   }
};
</script>


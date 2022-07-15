<script setup lang="ts">
const menus = [
  {
    title: 'Home',
    logo: '<div i-carbon:home inline-block />',
    link: '/',
  },
  {
    title: 'About Us',
    logo: '<div i-carbon:help-filled inline-block />',
    link: '/page/about-us',
  },
  {
    title: 'Contact',
    logo: '<div i-carbon:logo-discord inline-block />',
    link: '#',
  },
]
</script>

<template>
  <div>
    <section
      class="md:hidden block fixed bottom-0 inset-x-0 z-50 shadow-lg text-gray-200 bg-gray-700 dark:bg-dark backdrop-blur-lg bg-opacity-30 dark:bg-opacity-30 dark:text-gray-400 border-t-2 border-royal/20"
    >
      <div class="flex justify-between">
        <a
          v-for="(item, index) in menus" id="tabs" :key="index"
          :href="item.link"
          class="w-full focus:text-royal hover:text-royal justify-center inline-block text-center pt-2 pb-1 hover:bg-white hover:text-black"
          activeClass="dark:text-gray-100 text-black"
        >
          <span v-html="item.logo" />
          <span class="tab block text-xs">{{ item.title }}</span>
        </a>

        <!-- <a
          href="#"
          class="w-full focus:text-royal hover:text-royal justify-center inline-block text-center pt-2 pb-1 hover:bg-white"
          activeClass="dark:text-gray-100 text-black"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 inline-block mb-1" fill="none" viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M4 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2V6zM14 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V6zM4 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2v-2zM14 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2v-2z"
            />
          </svg>
          <span class="tab block text-xs">Categories</span>
        </a> -->

        <!-- <a
          href="#"
          class="w-full focus:text-royal hover:text-royal justify-center inline-block text-center pt-2 pb-1 hover:bg-white"
          activeClass="dark:text-gray-100 text-black"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 inline-block mb-1" fill="none" viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z"
            />
          </svg>
          <span class="tab block text-xs">CONTACT</span>
        </a>

        <a
          href="#"
          class="w-full focus:text-royal hover:text-royal justify-center inline-block text-center pt-2 pb-1 hover:bg-gray-300"
          activeClass="dark:text-gray-100 text-black"
        >
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 inline-block mb-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
          </svg>
          <span class="tab block text-xs">About</span>
        </a>
         -->
      </div>
    </section>
  </div>
</template>

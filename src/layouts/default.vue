<script setup lang="ts">
// const title = import.meta.env.VITE_SITE_NAME
// const logo_url = import.meta.env.VITE_SITE_LOGO
// const show_menu = true
// const handleMenuButton = () => {
//   !show_menu
// }
</script>

<template>
  <main class="xl:w-1/2 lg:w-2/3 w-full px-4 py-10 m-auto rounded shadow-lg bg-cool-gray-900 shadow-gray-400 text-center text-white dark:text-white">
    <RouterView />
    <Footer />
    <div class="mt-5 mx-auto text-center opacity-75 dark:opacity-50 text-sm" />
    <BottomNav />
  </main>
</template>

<script setup lang="ts">
const { t, availableLocales, locale } = useI18n()

const toggleLocales = () => {
  // change to some real logic
  const locales = availableLocales
  locale.value = locales[(locales.indexOf(locale.value) + 1) % locales.length]
}
</script>

<template>
  <div class="hidden md:block">
    <nav class="text-xl mt-6 ">
      <RouterLink class="icon-btn mx-2" to="/" :title="t('button.home')">
        About Us
      </RouterLink>
      -
      <RouterLink class="icon-btn mx-2" to="/" :title="t('button.home')">
        Contact Us
      </RouterLink>
      -
      <RouterLink class="icon-btn mx-2" to="/" :title="t('button.home')">
        Privacy Policy
      </RouterLink>
    </nav>
  </div>
</template>

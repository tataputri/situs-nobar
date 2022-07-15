<script setup lang="ts">
const env = import.meta.env
</script>

<template>
  <div>
    <div text-4xl>
      <div i-carbon-campsite inline-block />
    </div>
    <p>
      <a rel="noreferrer" href="https://github.com/antfu/vitesse" class="text-3xl text-red-600" target="_blank">
        {{ env.VITE_SITE_NAME }}
      </a>
    </p>
  </div>
</template>

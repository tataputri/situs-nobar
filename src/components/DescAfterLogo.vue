<script setup lang="ts">
const props = defineProps<{
  title: String
}>()
</script>

<template>
  <div>
    <p>
      <em text-sm opacity-75>{{ props.title }}</em>
    </p>
  </div>
</template>


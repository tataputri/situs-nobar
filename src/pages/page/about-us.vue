<script setup lang="ts">
const { t } = useI18n()
const discord = import.meta.env.VITE_CONTACT_DISCORD
const meta = {
  title: `Tentang ${t('site.title')}`,
  desc: `Deskripsi ${t('site.title')}`,
  siteurl: import.meta.env.VITE_SITE_URL,

}

useHead({
  title: meta.title,
  meta: [
    { name: 'description', content: meta.desc },
    {
      name: 'theme-color',
      content: computed(() => isDark.value ? '#00aba9' : '#ffffff'),
    },
  ],
  link: [
    {
      rel: 'icon',
      type: 'image/svg+xml',
      href: computed(() => preferredDark.value ? '/favicon-dark.svg' : '/favicon.svg'),
    },
  ],
})
</script>

<template>
  <div>
    <LogoUtama />
    <DescAfterLogo :title="meta.title" />
    <div class="py-4" />

    <strong class="text-red-400">{{ meta.siteurl }}</strong> merupakan situs yang menyediakan informasi mengenai penyedia atau provider dari acara nonton bareng yang ada di Indonesia.

    <div class="py-2" />
    <strong class="text-red-400">{{ meta.siteurl }}</strong> juga menyediakan informasi mengenai <strong>Link Alternatif</strong> dari berbagai provider nonton bareng (Nobar) sehingga para pembaca dapat dengan mudah mengakses situs-situs tersebut.

    Data yang kami sajikan disini kami dapatkan dari berbagai mesin pencari dan beberapa submisi dari para pembaca kami, jika pemilik situs merasa keberatan website / situsnya kami masukkan kedalam website <strong class="text-red-400">{{ meta.siteurl }}</strong> silahkan langsung hubugi kami di
    <div i-carbon:logo-discord inline-block /> {{ discord }}
  </div>
</template>

<route lang="yaml">
meta:
  layout: default
</route>

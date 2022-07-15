<script setup lang="ts">
const user = useUserStore()
const name = $ref(user.savedName)
const env = import.meta.env

const router = useRouter()
const go = () => {
  if (name)
    router.push(`/hi/${encodeURIComponent(name)}`)
}

const { t } = useI18n()
useHead({
  title: t('site.title'),
  meta: [
    { name: 'description', content: t('site.desc') },
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

    <DescAfterLogo :title="env.VITE_SITE_DESC" />

    <div py-4 />
    <div class="">
      <p>Nonton Bareng merukapan sebuah kegiatan yang sering sekali dilakukan oleh orang orang dari berbagai belahan dunia, baik dalam negeri ataupun luar negeri. Di Indonesia sendiri Nonton Bareng banyak di lakukan apabila ada pertandingan besar ataupun team besar yang sedang bermain.</p>
      <div class="py-4" />

      <p>Jenis olahraga yang sering dijadikan tontonan untuk nonton bareng bervariasi, tetapi olahraga Sepakbola mendominasi kegiatan <strong>Nonton Bareng</strong> ini, dikarenakan mayoritas orang Indonesia sangat menyukai olahraga sepakbola, baik muda ataupun tua, baik orang desa ataupun orang kota, semua menyukai olahraga ini </p>
      <div class="py-4" />
      <p><strong>Nonton Bareng</strong> seringnya dilakukan di cafe-cafe ataupun tempat umum lainnya, tergantung dari pihak penyelenggara <strong>Nonton Bareng</strong> tersebut. Hal ini tidak terbatas pada penyelenggara saja, siapa saja dapat melakukan melaksanakan kegiatan <strong>Nonton Bareng</strong> ini.</p>
      <div class="py-4" />
      <p>Berikut kami sajikan beberapa website yang mengadakan <strong>Situs Nonton Bareng</strong></p>
    </div>

    <HomeList />
  </div>
</template>


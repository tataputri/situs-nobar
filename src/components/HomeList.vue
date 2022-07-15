<script setup lang="ts">
import axios from 'axios'
import { useAxios } from '@vueuse/integrations/useAxios'

const instance = axios.create({
  baseURL: 'https://cors.livestreamapi.xyz/https://exp.cuan.dev',
  // baseURL: "https://exp.cuan.dev",
  headers: {
    'Content-type': 'application/json',
  },
})

const { data } = useAxios('/api/situs-nobar-lists', { method: 'GET' }, instance)
const nobarSiteList = data

// const xxx = [
//   {
//     name: 'BGIBOLA',
//     poster: 'https://situsnobar.com/wp-content/uploads/2021/07/Bgibola.jpg',
//     link: 'https://bgibola1.bar/',
//   },
//   {
//     name: 'BOLASIAR',
//     poster: 'https://situsnobar.com/wp-content/uploads/2021/07/bolasiar.jpg',
//     link: 'https://159.65.130.151/',
//   },
//   {
//     name: 'TVBERSAMA',
//     poster: 'https://situsnobar.com/wp-content/uploads/2021/07/tvbersama.jpg',
//     link: 'https://45.32.112.163/',
//   },
// ]
</script>

<template>
  <div>
    <div v-if="nobarSiteList" id="nobar-site-list" class="flex flex-col items-center">
      <div class="flex flex-col container max-w-md mt-10 mx-auto w-full items-center justify-center bg-light-blue-900 rounded-sm shadow">
        <ul class="flex flex-col divide-y w-full">
          <li v-for="(item, index) in nobarSiteList" :key="index" class="flex flex-row">
            <div class="select-none cursor-pointer hover:bg-gray-900 flex flex-1 items-center p-4">
              <div class="flex flex-col w-10 h-10 justify-center items-center mr-4">
                <a href="#" class="block relative">
                  <img alt="profil" :src="item.poster" class="mx-auto object-cover rounded-full h-10 w-10">
                </a>
              </div>
              <div class="flex-1 pl-1">
                <div class="font-medium dark:text-white">
                  {{ item.name }}
                </div>
                <div class="text-gray-600 dark:text-gray-200 text-sm" />
              </div>
              <div class="flex flex-row justify-center">
                <div class="text-gray-600 dark:text-gray-200 text-xs" />
                <button class="w-10 text-right flex justify-end">
                  <svg width="20" fill="currentColor" height="20" class="hover:text-gray-800 dark:hover:text-white dark:text-gray-200 text-gray-500" viewBox="0 0 1792 1792" xmlns="http://www.w3.org/2000/svg">
                    <path d="M1363 877l-742 742q-19 19-45 19t-45-19l-166-166q-19-19-19-45t19-45l531-531-531-531q-19-19-19-45t19-45l166-166q19-19 45-19t45 19l742 742q19 19 19 45t-19 45z" />
                  </svg>
                </button>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
    <div v-else />
  </div>
</template>

<script setup lang="ts">
import { meta, getUrl } from '@/utils'

const description = 'Learn about Color Xpret, a powerful color tool for designers and developers.'
const url = getUrl('/about')

useSeoMeta({
  title: 'About',
  description,
  ogUrl: url,
  ogTitle: 'About - Color Xpret',
  ogDescription: description,
  ogImageAlt: meta.alt,
  twitterTitle: 'About - Color Xpret',
  twitterDescription: description,
  twitterImageAlt: meta.alt,
})

useHead({
  link: [{ rel: 'canonical', href: url }],
})

defineOgImageComponent('NuxtSeo', {
  title: 'About - Color Xpret',
  description: description,
  siteName: 'Color Xpret',
  siteLogo: meta.logo,
  theme: '#187bff',
})

const techs = [
  { name: 'Nuxt', link: 'https://Nuxt.com/' },
  { name: 'Vue', link: 'https://vuejs.org/' },
  { name: 'TailwindCSS', link: 'https://tailwindcss.com/' },
  { name: 'TinyColor', link: 'https://github.com/scttcper/tinycolor' },
  { name: 'Chroma-js', link: 'https://github.com/gka/chroma.js' },
  { name: 'Reka UI', link: 'https://reka-ui.com/' },
  { name: 'Vue3 Toastify', link: 'https://vue3-toastify.js-bridge.com/' },
]
</script>

<template>
  <article class="min-h-screen pt-4 md:pt-8">
    <div class="mx-auto max-w-5xl">
      <div class="mb-4 px-2 text-center md:mb-8">
        <h1>About Color Xpret</h1>
      </div>
      <div class="sec max-w-3xl">
        <section id="intro" class="mb-8">
          <p class="text-lg leading-relaxed">
            <strong>Color Xpret</strong> is a comprehensive color tool designed for designers and
            developers. It combines essential <i>color manipulation features</i> into a single but
            efficient platform, providing color insights, format conversion, and modification
            capabilities.
          </p>
        </section>
        <section id="techs">
          <h2>Credits</h2>
          <p class="mt-4 mb-2 text-lg">Built with the following amazing technologies:</p>
          <ul class="flex flex-row flex-wrap gap-2">
            <li v-for="tech in techs" :key="tech.name">
              <a
                :href="tech.link"
                target="_blank"
                rel="noopener nofollow"
                class="inline-flex items-center rounded-lg bg-gray-200 px-4 py-2 text-lg hover:bg-gray-300 focus:ring-2 focus:ring-primary focus:ring-offset-2 focus:outline-none dark:bg-gray-800 dark:hover:bg-gray-700"
                :aria-label="'Learn more about ' + tech.name"
              >
                {{ tech.name }}
              </a>
            </li>
          </ul>
        </section>
      </div>
    </div>
  </article>
</template>

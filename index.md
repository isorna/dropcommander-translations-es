---
layout: 'home'
lang: 'es-ES'
title: 'Inicio'
hero:
  name: 'Drop Commander'
  text: 'Universo'
  tagline: 'Hecho por fans, para fans.'
features:
  - title: 'Dropfleet Commander V1.7.0'
    link: './dfc/'
    details: 'Reglas actualizadas de Dropfleet Commander y FAQ v2.6.1.'
    icon:
      light: '/img/ui/orbit.png'
      dark: '/img/ui/orbit.dark.png'
      width: '100px'
      height: '100px'
  - title: 'Dropzone Commander V2.2.0'
    link: './dzc/'
    details: 'Reglas actualizadas de Dropzone Commander y FAQ v2.4.'
    icon:
      light: '/img/ui/moon-landing.png'
      dark: '/img/ui/moon-landing.dark.png'
      width: '100px'
      height: '100px'
---
<script lang="ts" setup>
import { onMounted } from 'vue'
import { useData } from 'vitepress'
const { frontmatter } = useData()

onMounted(() => {
  let expires = new Date()
  expires.setFullYear(expires.getFullYear()+1)
  document.cookie = `nf_lang=${frontmatter.value.lang}; expires=${expires.toUTCString()}; path=/`
})
</script>

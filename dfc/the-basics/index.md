---
title: 'Lo básico'
excerpt: 'Reglas básicas de Dropfleet Commander.'
position: 3
---
# {{ $frontmatter.title }}

<script setup>
  import { data as pages } from '/documents.data'
  const slug = '/es/dfc/the-basics/'
  const filteredPages = pages.filter(page => page?.href.indexOf(slug) > -1
      && page?.href.indexOf('index.html') < 0
      && !page?.href.endsWith('/'))
    .sort((a, b) => a.position - b.position)
</script>

<CategoryCardsContainer :pages="filteredPages" />

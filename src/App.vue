<script>
export default {
  data() {
    return {
      techs: [
        { name: 'Vue', link: 'https://vuejs.org/' },
        { name: 'Vite', link: 'https://vitejs.dev/' },
        { name: 'Tailwind', link: 'https://tailwindcss.com/' },
        { name: 'Catppuccin', link: 'https://tailwindcss.catppuccin.com/' },
        { name: 'Github Pages', link: 'https://pages.github.com/'},
      ]
    }
  }
}
</script>

<template>
  <div class="flex items-center justify-center min-h-screen">
    <h1 class="text-3xl text-gradient from-green via-sapphire to-mauve">
      <span v-for="(tech, i) in techs">
        <span v-if="i"> + </span>
        <a :href="tech.link" target="_blank" class="font-extrabold">{{ tech.name }}</a>
      </span>
    </h1>
  </div>
</template>
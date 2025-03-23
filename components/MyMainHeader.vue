<template>
  <div class="flex flex-row items-center justify-between mb-6">
    <p class="text-2xl">Raksa Meth</p>
    <div class="flex flex-row gap-4">
      <div><NuxtLink to="/">Home</NuxtLink></div>
      <div><NuxtLink to="/about">About</NuxtLink></div>
      <div> <NuxtLink to="/projects">Projects</NuxtLink></div>
    </div>
    <ClientOnly>
      <div :class="['w-16  rounded-full p-1 border',colorMode.preference == 'dark'? 'bg-slate-700 border-slate-500':'bg-orange-100 border-orange-500']">
        <input type="checkbox" class="hidden">
        <div ref="darkModeSlider" :class="['w-6 h-6 cursor-pointer transition-all ease-in-out  rounded-full',colorMode.preference == 'dark'?'translate-x-8 bg-blue-200':'bg-orange-400']" v-on:click="toggleColor"></div>
    </div>
    </ClientOnly>
    
    
  </div>
</template>

<script lang="ts" setup>

const darkModeSlider = ref<HTMLDivElement>();
const colorMode = useColorMode();

const toggleColor = () => {
  colorMode.preference = colorMode.preference == "dark" ? "light" : "dark";
}


</script>

<style>

</style>
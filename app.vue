<template>
  <div :class="[' px-80 pt-10 min-h-screen .${color}-mode',colorMode.preference == 'dark'?'bg-slate-900 text-cyan-100':'bg-orange-50']">
    <NuxtLayout>
      <NuxtPage/>
    </NuxtLayout>
    
  </div>
</template>

<script setup lang="ts">
  const colorMode = useColorMode();
</script>
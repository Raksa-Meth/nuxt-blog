<template>
  <div>
    <h1>Projects</h1>

    <div v-if="status === 'pending'">Loading...</div>
    <div v-else-if="status === 'error'">Error: {{ error }}</div>
    <div v-else class="mt-4">
       <div v-for="currentData in data" :key="currentData.id">
        {{ currentData.name }}
      </div>>
    </div>
  </div>
</template>

<script lang="ts" setup>
  const { data, status , error, refresh } = await useFetch<any>('https://api.github.com/users/piotr-jura-udemy/repos',{
  })


</script>

<style>

</style>
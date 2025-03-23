<template>
    <div class=" mt-2">
      <ContentRenderer v-if="content" :value="content"></ContentRenderer>
    </div>
</template>

<script lang="ts" setup>

const route = useRoute()
const blogContentStringPath = route.path.split("blog")[1]?.trim().split(" ")[0];


const { data: content } = await useAsyncData(blogContentStringPath, () => {
    return queryCollection('content').path(blogContentStringPath).first()
})

</script>
<template>
    <div>
        <h1>Home</h1>
    </div>
</template>

<script setup lang="ts">

const colorMode = useColorMode();
colorMode.preference = "dark";

definePageMeta({
    middleware:'home-middleware',
});

</script>

<style scoped>

</style>
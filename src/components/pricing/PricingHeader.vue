<script setup>
    defineProps({
        title:String,
        subTitle:String,
    })
</script>

<template>
    <div class="mx-auto max-w-screen-md text-center mb-8 lg:mb-12">
        <h2 class="mb-4 text-4xl tracking-tight font-extrabold text-gray-900 dark:text-white">{{ title }}</h2>
        <p class="mb-5 font-light text-gray-500 sm:text-xl dark:text-gray-400">{{ subTitle }}</p>
    </div>
</template>

<style scoped>

</style>
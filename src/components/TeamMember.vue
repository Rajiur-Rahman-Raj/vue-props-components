<script setup>
// defineProps([
//     'name'
// ])

defineProps([
    'name',
    'designation',
    'description',
    'image',
    'socials',
])


</script>

<template>
<div class="items-center bg-gray-50 shadow sm:flex dark:bg-gray-800 dark:border-gray-700">
    <a href="#">
        <img class="w-full  " :src="image" :alt="name">
    </a>
    <div class="p-5">
        <h3 class="text-xl font-bold tracking-tight text-gray-900 dark:text-white">
            <a href="#">{{ name }}</a>
        </h3>
        <span class="text-gray-500 dark:text-gray-400">{{ designation }}</span>
        <p class="mt-3 mb-4 font-light text-gray-500 dark:text-gray-400">{{ description }}</p>
        <ul class="flex space-x-4 sm:mt-0">
            <li v-for="(social, index) in socials" :key="index">
                <a href="#" class="text-gray-500 hover:text-gray-900 dark:hover:text-white">
                    <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                                    <path fill-rule="evenodd" :d="social.icon" clip-rule="evenodd" />
                                                </svg>
                </a>
            </li>
            
        </ul>
    </div>
</div>
</template>

<style scoped>

</style>
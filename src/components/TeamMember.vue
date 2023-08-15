<script setup>
   defineProps({
    title: String,
    subtitle: String,
    persons: Array,
   })
</script>

<template>
<div class="py-8 px-4 mx-auto max-w-screen-xl lg:py-16 lg:px-6 ">
        <div class="mx-auto max-w-screen-sm text-center mb-8 lg:mb-16">
          <h2 class="mb-4 text-4xl tracking-tight font-extrabold text-gray-900 dark:text-white">{{ title }}</h2>
          <p class="font-light text-gray-500 lg:mb-16 sm:text-xl dark:text-gray-400">{{ subtitle }}</p>
        </div>
        <div class="grid gap-8 mb-6 lg:mb-16 md:grid-cols-2">
            <div class="items-center bg-gray-50 shadow sm:flex dark:bg-gray-800 dark:border-gray-700" v-for="(person, index) in persons" :key="index">
    <a href="#">
        <img class="w-full  " :src="person.image" :alt="name">
    </a>
    <div class="p-5">
        <h3 class="text-xl font-bold tracking-tight text-gray-900 dark:text-white">
            <a href="#">{{ person.name }}</a>
        </h3>
        <span class="text-gray-500 dark:text-gray-400">{{ person.designation }}</span>
        <p class="mt-3 mb-4 font-light text-gray-500 dark:text-gray-400">{{ person.description }}</p>
        <ul class="flex space-x-4 sm:mt-0">
            <li v-for="(social, index) in person.socials" :key="index">
                <a href="#" class="text-gray-500 hover:text-gray-900 dark:hover:text-white">
                    <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                                                    <path fill-rule="evenodd" :d="social.icon" clip-rule="evenodd" />
                                                </svg>
                </a>
            </li>
            
        </ul>
    </div>
</div>
        </div>
      </div>


</template>

<style scoped>

</style>
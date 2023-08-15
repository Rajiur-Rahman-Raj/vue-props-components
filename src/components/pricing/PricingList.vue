<script setup>
    defineProps({
        buttonText:String,
        packages:Array,
    })
</script>

<template>
    <!-- Pricing Card -->
    <div class="flex flex-col p-6 mx-auto max-w-lg text-center text-gray-900 bg-white rounded-lg border border-gray-100 shadow dark:border-gray-600 xl:p-8 dark:bg-gray-800 dark:text-white" v-for="(pack, index) in packages" :key="index">
        <h3 class="mb-4 text-2xl font-semibold">{{ pack.title }}</h3>
        <p class="font-light text-gray-500 sm:text-lg dark:text-gray-400">{{ pack.subTitle }}</p>
        <div class="flex justify-center items-baseline my-8">
            <span class="mr-2 text-5xl font-extrabold">{{ pack.currencySymbol }}{{ pack.price }}</span>
            <span class="text-gray-500 dark:text-gray-400">/{{ pack.date }}</span>
        </div>
        <!-- List -->
        <ul role="list" class="mb-8 space-y-4 text-left">
            <li class="flex items-center space-x-3" v-for="(list, index) in pack.lists" :key="index">
                <!-- Icon -->
                <i :class="list.isChecked == true ? 'fas fa-check' : 'fas fa-times'"></i>
               
                
                
                <span>{{ list.title }}</span>
            </li>
        </ul>
        <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
                  Button
                </button>
    </div>
</template>

<style scoped>

</style>
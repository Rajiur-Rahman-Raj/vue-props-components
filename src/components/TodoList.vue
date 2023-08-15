<script setup>
    defineProps({
        tasks: Array,
    })
</script>

<template>
    <div class="flex flex-grow items-center justify-center h-full text-gray-600 bg-gray-100">
        <!-- Component Start -->
        <div class="max-w-full p-8 rounded-lg shadow-lg w-96" :class="tasks[0].background">
            <div class="flex items-center mb-6">
                <svg class="h-8 w-8 text-indigo-500 stroke-current" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20 13V6a2 2 0 00-2-2H6a2 2 0 00-2 2v7m16 0v5a2 2 0 01-2 2H6a2 2 0 01-2-2v-5m16 0h-2.586a1 1 0 00-.707.293l-2.414 2.414a1 1 0 01-.707.293h-3.172a1 1 0 01-.707-.293l-2.414-2.414A1 1 0 006.586 13H4"></path>
                                    </svg>
                <h4 class="font-semibold ml-3 text-lg">Frodo's Jobs</h4>
            </div>
            <div v-for="(list, index) in tasks[0].lists" :key="index">
                <input class="hidden" type="checkbox" :id="`task${index}`" :checked="list.status" >
                <label class="flex items-center h-10 px-2 rounded cursor-pointer hover:bg-gray-100" :for="`task${index}`">
                                      <span class="flex items-center justify-center w-5 h-5 text-transparent border-2 border-gray-300 rounded-full">
                                        <svg class="w-4 h-4 fill-current" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
                                          <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                                        </svg>
                                      </span>
                                      <span class="ml-4 text-sm">{{ list.task }}.</span>
                                    </label>
            </div>
        </div>
        <!-- Component End  -->
    </div>
    <div class="flex flex-grow items-center justify-center bg-gray-900 h-full">
        <!-- Component Start -->
        <div class="max-w-full p-8  rounded-lg shadow-lg w-96 text-gray-200" :class="tasks[1].background">
            <div class="flex items-center mb-6">
                <svg class="h-8 w-8 text-indigo-500 stroke-current" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20 13V6a2 2 0 00-2-2H6a2 2 0 00-2 2v7m16 0v5a2 2 0 01-2 2H6a2 2 0 01-2-2v-5m16 0h-2.586a1 1 0 00-.707.293l-2.414 2.414a1 1 0 01-.707.293h-3.172a1 1 0 01-.707-.293l-2.414-2.414A1 1 0 006.586 13H4"></path>
                                    </svg>
                <h4 class="font-semibold ml-3 text-lg">Sam's Jobs</h4>
            </div>
            <div v-for="(list, index) in tasks[0].lists" :key="index">
                <input class="hidden" type="checkbox" :id="`task${list.task}`" :checked="list.status">
                <label class="flex items-center h-10 px-2 rounded cursor-pointer hover:bg-gray-900" :for="`task${list.task}`">
                                      <span class="flex items-center justify-center w-5 h-5 text-transparent border-2 border-gray-500 rounded-full">
                                        <svg class="w-4 h-4 fill-current" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
                                          <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                                        </svg>
                                      </span>
                                      <span class="ml-4 text-sm">{{ list.task }}</span>
                                    </label>
            </div>
        </div>
        <!-- Component End  -->
    </div>
</template>

<style>
    input[type=checkbox]:checked+label span:first-of-type {
        background-color: #10B981;
        border-color: #10B981;
        color: #fff;
    }
    input[type=checkbox]:checked+label span:nth-of-type(2) {
        text-decoration: line-through;
        color: #9CA3AF;
    }
</style>

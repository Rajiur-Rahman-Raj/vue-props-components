<script setup>
    import TodoList from "./components/TodoList.vue";

    const myTasks = [{
      title:"Frodo's Jobs",
      background: "bg-white",
      lists:[
        {
          task:"Weed front garden.",
          status: true,
        },
        {
          task:"Chill and smoke some Old Toby.",
          status: true,
        },
        {
          task:"Keep ring secret and safe.",
          status: false,
        },
        {
          task:"Meet Gandalf at Bree.",
          status: false,
        },
        {
          task:"Destroy ring and defeat dark lord.",
          status: false,
        },
    ]
    },
    {
      title:"Sam's Jobs",
      background: "bg-gray-800",
      lists:[
        {
          task:"Trim the verge.",
          status: true,
        },
        {
          task:"Eavesdrop on Master Frodo & Gandalf.",
          status: true,
        },
        {
          task:"Boil, mash, and stick potatoes in stew.",
          status: false,
        },
        {
          task:"Carry Frodo.",
          status: false,
        },
        {
          task:"Be all round legend.",
          status: false,
        },
    ]
    }
  ]

</script>

<template>
  <section class="mx-auto ">
    <h1 class="my-10 text-center">Components</h1>
    <div class="flex items-center justify-center h-[600px] font-medium">
      <TodoList :tasks="myTasks" background1="defaultBg1" background2="defaultBg2"/>
    </div>
  </section>
</template>

<style scoped>
  
</style>
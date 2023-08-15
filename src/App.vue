<script setup>
  
  import BookTicket from './components/BookTicket.vue'

  const topHeading = "Components"

  const bookingInfos = [{
    title:"The Magnificent Bogra",
    distance:"196 km",
    fromAddress:"from Dhaka",
    reviews:5,
    reviewCount:10,
    button:"Book Ticket",
    location:"*Places to visit: Mahasthangarh, Vasu Bihar & Momo Inn",
    image:"https://i.ibb.co/Kr4b0zJ/152013403-10158311889099633-8423107287930246533-o.jpg"
  },
  {
    title:"The Magnificent Bogra",
    subTitle:"Located in Rajshahi Division, Bogra is one of the oldest and most fascinating towns in Bangladesh",
    distance:"196 km",
    fromAddress:"from Dhaka",
    reviews:4,
    reviewCount:15,
    button:"Book Ticket",
    location:"*Places to visit: Mahasthangarh, Vasu Bihar & Momo Inn",
    image:"https://i.ibb.co/Kr4b0zJ/152013403-10158311889099633-8423107287930246533-o.jpg"
  }
]

</script>


<template>
  <section class="mx-auto ">
    <h1 class="my-10 text-center">{{ topHeading }}</h1>
    <div class="flex flex-col space-y-5">
      <BookTicket :bookinginformation="bookingInfos"/>
    </div>
  </section>
</template>

<style scoped>

</style>
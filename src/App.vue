<script setup>
    import PricingHeader from "./components/pricing/PricingHeader.vue";
    import PricingList from "./components/pricing/PricingList.vue";

    const title = "Designed for business teams like yours"
    const subTitle = "Here at Flowbite we focus on markets where technology, innovation, and capital can unlock long-term value and drive economic growth."
    const buttonText = "Get Started"
    const packages = [
      {
        title:"Starter",
        subTitle:"Best option for personal use & for your next project.",
        currencySymbol:"$",
        price:"99",
        date:"15 Days",
        lists:[
          {title:"Individual configuration", isChecked:true},
          {title:"No setup, or hidden fees", isChecked:true},
          {title:"Team size: 1 developer", isChecked:true},
          {title:"Premium support: 6 months", isChecked:false},
          {title:"Free updates: 6 months", isChecked:false},
        ],
      },
      {
        title:"Company",
        subTitle:"Best option for personal use & for your next project.",
        currencySymbol:"$",
        price:"99",
        date:"Monthly",
        lists:[
          {title:"Individual configuration", isChecked:true},
          {title:"No setup, or hidden fees", isChecked:false},
          {title:"Team size: 1 developer", isChecked:true},
          {title:"Premium support: 6 months", isChecked:false},
          {title:"Free updates: 6 months", isChecked:true},
        ],
      },
      {
        title:"Enterprise",
        subTitle:"Best option for personal use & for your next project.",
        currencySymbol:"$",
        price:"99",
        date:"Yearly",
        lists:[
          {title:"Individual configuration", isChecked:false},
          {title:"No setup, or hidden fees", isChecked:true},
          {title:"Team size: 1 developer", isChecked:false},
          {title:"Premium support: 6 months", isChecked:true},
          {title:"Free updates: 6 months", isChecked:true},
        ],
      },
    ]
</script>

<template>
  <section class="mx-auto ">
    <section class="bg-white dark:bg-gray-900">
      <div class="py-8 px-4 mx-auto max-w-screen-xl lg:py-16 lg:px-6">
        
        <PricingHeader :title="title" :subTitle="subTitle" />

        <div class="space-y-8 lg:grid lg:grid-cols-3 sm:gap-6 xl:gap-10 lg:space-y-0">
          <PricingList :buttonText="buttonText" :packages="packages"/>
        </div>
      </div>
    </section>
  </section>
</template>

<style scoped>
  
</style>
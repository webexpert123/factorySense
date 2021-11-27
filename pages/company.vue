<template>
<div>
  <div class="py-24 bg-gray-50 sm:py-32">
    <div class="max-w-md mx-auto pl-4 pr-8 sm:max-w-lg sm:px-6 lg:max-w-7xl lg:px-8">
      <h1 class="text-4xl leading-10 font-extrabold tracking-tight text-gray-900 text-center sm:text-5xl sm:leading-none lg:text-6xl">No one likes surprises.</h1>
      <p class="mt-6 max-w-3xl mx-auto text-xl leading-normal text-gray-500 text-center">When it comes to running a plant, surprises in missing inventory, lost kits, or misplaced assets mean downtime and lost revenue. End the chaos and drive huge ROI with FactorySense RFID.</p>
    </div>
  </div>
  <Stats1 />
</div>
</template>

<script>
import Stats1 from '@/components/Stats1'
export default {
  name: "Company",
  components: { Stats1 }
}
</script>

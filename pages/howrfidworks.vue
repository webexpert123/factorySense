<template>
<div>

  <!-- Page heading -->
  <div class="py-24 bg-gray-50 sm:py-32">
    <div class="max-w-md mx-auto pl-4 pr-8 sm:max-w-lg sm:px-6 lg:max-w-7xl lg:px-8">
      <h1 class="text-4xl leading-10 font-extrabold tracking-tight text-gray-900 text-center sm:text-5xl sm:leading-none lg:text-6xl">
        How Our Cloud-Based RFID System Works
      </h1>
      <p class="mt-6 max-w-3xl mx-auto text-xl leading-normal text-gray-500 text-center">
        A quick lesson on RFID systems, technologies, and options
      </p>
    </div>
  </div>
  <!-- /Page heading -->

  <LogoCloud />

</div>
</template>

<script>
import LogoCloud from '@/components/LogoCloud'
export default {
  name: "HowRFIDWorks",
  components: { LogoCloud }
}
</script>

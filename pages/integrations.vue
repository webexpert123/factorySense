<template>
  <div>
    <!-- Page heading -->
    <div class="py-24 bg-gray-50 sm:py-32">
      <div class="max-w-md mx-auto pl-4 pr-8 sm:max-w-lg sm:px-6 lg:max-w-7xl lg:px-8">
        <h1 class="text-4xl leading-10 font-extrabold tracking-tight text-gray-900 text-center sm:text-5xl sm:leading-none lg:text-6xl">
          RFID Is Better When It Works With Your System
        </h1>
        <p class="mt-6 max-w-3xl mx-auto text-xl leading-normal text-gray-500 text-center">
          Integrating with your existing environments allows FactorySense to deliver value faster and enables automation of many tasks.
        </p>
      </div>
    </div>
    <!-- End Page heading -->

    <!-- Narrative Section -->
    <div class="relative bg-white">
      <div class="lg:absolute lg:inset-0">
        <div class="lg:absolute lg:inset-y-0 lg:left-0 lg:w-1/2">
          <img class="h-56 w-full object-cover lg:absolute lg:h-full" src="~assets/images/office_worker_red.jpg" alt="">
        </div>
      </div>
      <div class="relative pt-12 pb-16 px-4 sm:pt-16 sm:px-6 lg:px-8 lg:max-w-7xl lg:mx-auto lg:grid lg:grid-cols-2">
        <div class="lg:col-start-2 lg:pl-8">
          <div class="text-base max-w-prose mx-auto lg:max-w-lg lg:ml-auto lg:mr-0">
            <h2 class="leading-6 text-indigo-600 font-semibold tracking-wide uppercase">Integrate RFID with your system</h2>
            <h3 class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl">We play nicely with others</h3>
            <div class="mt-5 prose prose-indigo text-gray-500">
              <p>Many of our customers maximize the value of their FactorySense RFID system by tying the realtime event data gathered from RFID sensors into other systems.</p>
              <p>Some of the transactions we can automate include:</p>
              <ul role="list">
                <li>Automate ERP transactions such as receipts, check-ins, and check-outs</li>
                <li>Automate transfers of material from one location to another</li>
                <li>Automate material consumption when workers take material from central stores</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- End Narrative Section -->

    <!-- Integration Count -->
    <div class="bg-gradient-to-tr from-gray-900 to-gray-700 text-center py-12">
      <h1 class="drop-shadow text-4xl tracking-tight font-extrabold text-indigo-50 sm:text-5xl md:text-6xl">
        180+
      </h1>
      <p class="drop-shadow mt-3 max-w-md mx-auto text-base text-gray-50 sm:text-lg md:mt-5 md:text-xl md:max-w-3xl">
        FactorySense currently integrates with over 180 third-party services, including most ERP platforms like SAP and Oracle, and SalesForce.
      </p>
    </div>
    <!-- End Integration Count -->
    <LogoCloud />

  </div>
</template>





<script>
import LogoCloud from '@/components/LogoCloud'
export default {
  name: "Integrations",
  components: { LogoCloud }
  // layout: 'abc' // by default it picks default.vue from layouts folder, it can be overridden here
}
</script>
<template>
  <footer class="bg-gray-50" aria-labelledby="footer-heading">
    <h2 id="footer-heading" class="sr-only">Footer</h2>
    <div class="max-w-7xl mx-auto pt-16 pb-8 px-4 sm:px-6 lg:pt-24 lg:px-8">
      <div class="mt-12 border-t border-gray-200 pt-8 md:flex md:items-center md:justify-between lg:mt-16">
        <nav class="-mx-5 -my-2 flex flex-wrap justify-center" aria-label="Footer">
      <div class="px-5 py-2">
        <a href="/terms-of-service" class="text-base text-gray-500 hover:text-gray-900">
          Terms of Sale &amp; Service
        </a>
      </div>

      <div class="px-5 py-2">
        <a href="/privacy-policy" class="text-base text-gray-500 hover:text-gray-900">
          Privacy Policy
        </a>
      </div>
    </nav>

        <p class="mt-8 text-base text-gray-400 md:mt-0 md:order-1">
          &copy; 2022 FactorySense RFID. All rights reserved.<br />
          Made with <span class="text-red-500">♥</span> in Dallas, Texas
        </p>
      </div>
    </div>
  </footer>
</template>
<script>
export default {
    name: 'Footer'
}
</script>
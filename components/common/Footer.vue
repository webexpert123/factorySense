<template>
     <footer class="bg-gray-50" aria-labelledby="footer-heading">
    <h2 id="footer-heading" class="sr-only">Footer</h2>
    <div class="max-w-7xl mx-auto pt-16 pb-8 px-4 sm:px-6 lg:pt-24 lg:px-8">
      <div class="xl:grid xl:grid-cols-3 xl:gap-8">
        <div class="grid grid-cols-2 gap-8 xl:col-span-2">
          <div class="md:grid md:grid-cols-2 md:gap-8">
            <div>
              <h3 class="text-sm font-semibold text-gray-400 tracking-wider uppercase">
                Solutions
              </h3>
              <ul role="list" class="mt-4 space-y-4">
                <li>
                  <a href="#" class="text-base text-gray-500 hover:text-gray-900">
                    Marketing
                  </a>
                </li>

                <li>
                  <a href="#" class="text-base text-gray-500 hover:text-gray-900">
                    Analytics
                  </a>
                </li>

                <li>
                  <a href="#" class="text-base text-gray-500 hover:text-gray-900">
                    Commerce
                  </a>
                </li>

                <li>
                  <a href="#" class="text-base text-gray-500 hover:text-gray-900">
                    Insights
                  </a>
                </li>
              </ul>
            </div>
            <div class="mt-12 md:mt-0">
              <h3 class="text-sm font-semibold text-gray-400 tracking-wider uppercase">
                Support
              </h3>
              <ul role="list" class="mt-4 space-y-4">
                <li>
                  <a href="#" class="text-base text-gray-500 hover:text-gray-900">
                    Integrations
                  </a>
                </li>

                <li>
                  <a href="#" class="text-base text-gray-500 hover:text-gray-900">
                    Documentation
                  </a>
                </li>

                <li>
                  <a href="#" class="text-base text-gray-500 hover:text-gray-900">
                    Guides
                  </a>
                </li>

                <li>
                  <a href="#" class="text-base text-gray-500 hover:text-gray-900">
                    API Status
                  </a>
                </li>
              </ul>
            </div>
          </div>
          <div class="md:grid md:grid-cols-2 md:gap-8">
            <div class="mt-12 md:mt-0">
              <h3 class="text-sm font-semibold text-gray-400 tracking-wider uppercase">
                Legal
              </h3>
              <ul role="list" class="mt-4 space-y-4">
                <li>
                  <a href="/terms-of-service" class="text-base text-gray-500 hover:text-gray-900">
                    Terms of Service
                  </a>
                </li>

                <li>
                  <a href="/privacy-policy" class="text-base text-gray-500 hover:text-gray-900">
                    Privacy Policy
                  </a>
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="mt-12 xl:mt-0">
          <h3 class="text-sm font-semibold text-gray-400 tracking-wider uppercase">
            Subscribe to our newsletter
          </h3>
          <p class="mt-4 text-base text-gray-500">
            The latest news, articles, and resources, sent to your inbox weekly.
          </p>
          <form class="mt-4 sm:flex sm:max-w-md">
            <label for="email-address" class="sr-only">Email address</label>
            <input id="email-address" type="email"  name="email-address"  autocomplete="email" required class="appearance-none min-w-0 w-full bg-white border border-gray-300 rounded-md shadow-sm py-2 px-4 text-base text-gray-900 placeholder-gray-500 focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 focus:placeholder-gray-400" placeholder="Enter your email">
            <div class="mt-3 rounded-md sm:mt-0 sm:ml-3 sm:flex-shrink-0">
              <button type="submit" class="w-full flex items-center justify-center bg-gradient-to-r from-purple-600 to-indigo-600 bg-origin-border px-4 py-3 border border-transparent text-base font-medium rounded-md shadow-sm text-white hover:from-purple-700 hover:to-indigo-700">
                Subscribe
              </button>
            </div>
          </form>
        </div>
      </div>
      <div class="mt-12 border-t border-gray-200 pt-8 md:flex md:items-center md:justify-between lg:mt-16">
        <!-- Right Aligned Logos -->
        <div class="flex space-x-6 md:order-2">
          <a href="#" class="text-gray-400 hover:text-gray-500">
            <span class="sr-only">Facebook</span>
            <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
              <path fill-rule="evenodd" d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z" clip-rule="evenodd" />
            </svg>
          </a>
        </div>
        <!-- End Right Aligned Logos -->

        <p class="mt-8 text-base text-gray-400 md:mt-0 md:order-1">
          &copy; 2021 FactorySense RFID. All rights reserved.<br />
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
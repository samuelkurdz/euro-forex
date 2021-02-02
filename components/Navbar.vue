<template>
  <nav :class="{ 'scrolled': !view.atTopOfPage }" class="fixed w-full bg-gray-800 m-auto top-0 animated">
    <div class="max-w-7xl mx-auto px-2 sm:px-6 lg:px-8">
      <div class="relative flex items-center justify-between h-16">
        <div class="absolute inset-y-0 left-0 flex items-center lg:hidden">
          <!-- Mobile menu button-->
          <button @click="toggleMenu" class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-white hover:bg-gray-700 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white" aria-expanded="false">
            <span class="sr-only">Open main menu</span>
            <!-- Icon when menu is closed. -->
            <!--
              Heroicon name: menu
              Menu open: "hidden", Menu closed: "block"
            -->
            <svg :class="isOpen ? 'hidden' : 'block'" class="h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
            <!-- Icon when menu is open. -->
            <!--
              Heroicon name: x
              Menu open: "block", Menu closed: "hidden"
            -->
            <svg :class="isOpen ? 'block' : 'hidden'" class="h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
        <div class="flex-1 flex items-center justify-center lg:items-stretch lg:justify-between">
          <div class="flex-shrink-0 flex items-center">
            <NuxtLink tag="a" to="/"><img class="block lg:hidden h-8 w-auto" src="https://tailwindui.com/img/logos/workflow-mark-indigo-500.svg" alt="Workflow"></NuxtLink>
            <NuxtLink tag="a" to="/"><img class="hidden lg:block h-8 w-auto" src="https://tailwindui.com/img/logos/workflow-logo-indigo-500-mark-white-text.svg" alt="Workflow"></NuxtLink>
          </div>
          <div class="hidden lg:block sm:ml-6">
            <div class="flex space-x-4">
              <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
              <a href="#" class="relative dropdown-title text-gray-300 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-sm font-medium inline-flex">
                Regulated Broker
                <svg class="-mr-1 ml-2 h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                  <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
                </svg>
                <ul class="dropdown-menu absolute right-0 text-gray-700 pt-8 hidden">
                  <li class=""><NuxtLink  class="rounded-t bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" to="/regulated_brokers/FCA" tag="a">FCA Brokers</NuxtLink></li>
                  <li class=""><NuxtLink class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" to="/regulated_brokers/Cysec" tag="a">Cysec Brokers</NuxtLink></li>
                  <li class=""><NuxtLink class="rounded-b bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" to="/regulated_brokers/ASIC" tag="a">ASIC Brokers</NuxtLink></li>
                  <li class=""><NuxtLink class="rounded-b bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" to="/regulated_brokers/FSCA" tag="a">FSCA Brokers</NuxtLink></li>
                </ul>
              </a>
              <a href="#" class="relative dropdown-title text-gray-300 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-sm font-medium inline-flex">
                Brokers Review
                <svg class="-mr-1 ml-2 h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                  <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
                </svg>
                <ul class="dropdown-menu absolute right-0 text-gray-700 pt-8 hidden">
                  <li class=""><a class="rounded-t bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Moneta Market Review</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Vantage FA Reviews</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Plus 500 Reviews</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Easy Market Reviews</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Pepperstone Reviews</a></li>
                  <li class=""><a class="rounded-b bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Fp Market Reviews</a></li>
                </ul>
              </a>
              <a href="#" class="relative dropdown-title text-gray-300 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-sm font-medium inline-flex">
                Brokers by Trading Account
                <svg class="-mr-1 ml-2 h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                  <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
                </svg>
                <ul class="dropdown-menu absolute right-0 text-gray-700 pt-8 hidden">
                  <li class=""><a class="rounded-t bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Demo Account Brokers</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Hedging Account Brokers</a></li>
                  <li class=""><a class="rounded-b bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Islamic Account Brokers</a></li>
                </ul>
              </a>
              <a href="#" class="relative dropdown-title text-gray-300 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-sm font-medium inline-flex">
                Brokers by Trading Platform
                <svg class="-mr-1 ml-2 h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                  <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
                </svg>
                <ul class="dropdown-menu absolute right-0 text-gray-700 pt-8 hidden">
                  <li class=""><a class="rounded-t bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Auto Trading Platforms</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Copy Trading Platforms</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">MT4 Platforms</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">MT5 Platforms</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Social Trading Platforms</a></li>
                  <li class=""><a class="rounded-b bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Web Traders</a></li>
                </ul>
              </a>
              <a href="#" class="relative dropdown-title text-gray-300 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-sm font-medium inline-flex">
                Instruments offered by Brokers
                <svg class="-mr-1 ml-2 h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                  <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
                </svg>
                <ul class="dropdown-menu absolute right-0 text-gray-700 pt-8 hidden">
                  <li class=""><a class="rounded-t bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Stock</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">CFD</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Commodities</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">ETFs</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Gold</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Oil</a></li>
                  <li class=""><a class="rounded-b bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Silver</a></li>
                </ul>
              </a>
              <a href="#" class="relative dropdown-title text-gray-300 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-sm font-medium inline-flex">
                Brokers by Countries
                <svg class="-mr-1 ml-2 h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                  <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
                </svg>
                <ul class="dropdown-menu absolute right-0 text-gray-700 pt-8 hidden">
                  <li class=""><a class="rounded-t bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">African Forex Brokers</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Asian Forex Brokers</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Australia Forex Brokers</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">EU Forex Brokers</a></li>
                  <li class=""><a class="rounded-b bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">UK Forex Brokers</a></li>
                </ul>
              </a>
              <a href="#" class="text-gray-300 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-sm font-medium">Education</a>
              <a href="#" class="relative dropdown-title text-gray-300 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-sm font-medium inline-flex">
                News
                <svg class="-mr-1 ml-2 h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                  <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
                </svg>
                <ul class="dropdown-menu absolute right-0 text-gray-700 pt-8 hidden">
                  <li class=""><a class="rounded-t bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Stock News</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Bitcoin News</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Oil News</a></li>
                  <li class=""><a class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Gold News</a></li>
                  <li class=""><a class="rounded-b bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" href="#">Etherium News</a></li>
                </ul>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!--
      Mobile menu, toggle classes based on menu state.
      Menu open: "block", Menu closed: "hidden"
    -->
    <div :class="isOpen ? 'block' : 'hidden' " class="lg:hidden">
      <div class="px-2 pt-2 pb-3 space-y-1">
        <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
        <a href="#" class="bg-gray-900 text-white block px-3 py-2 rounded-md text-base font-medium">
          Regulated Brokers
<!--          <ul class="dropdown-menu absolute right-0 text-gray-700 pt-8 hidden">-->
<!--            <li class=""><NuxtLink  class="rounded-t bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" to="/regulated_brokers/FCA" tag="a">FCA Brokers</NuxtLink></li>-->
<!--            <li class=""><NuxtLink class="bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" to="/regulated_brokers/Cysec" tag="a">Cysec Brokers</NuxtLink></li>-->
<!--            <li class=""><NuxtLink class="rounded-b bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" to="/regulated_brokers/ASIC" tag="a">ASIC Brokers</NuxtLink></li>-->
<!--            <li class=""><NuxtLink class="rounded-b bg-gray-200 hover:bg-gray-400 py-2 px-4 block whitespace-no-wrap" to="/regulated_brokers/FSCA" tag="a">FSCA Brokers</NuxtLink></li>-->
<!--          </ul>-->
        </a>
        <a href="#" class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Brokers Review</a>
        <a href="#" class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Brokers By Trading Account</a>
        <a href="#" class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Brokers By Trading Platform</a>
        <a href="#" class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Instruments Offered By Brokers</a>
        <a href="#" class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Brokers By Countries</a>
        <a href="#" class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Education</a>
        <a href="#" class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium">News</a>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
name: "Navbar",
  data () {
    return {
      isOpen: true,
      view: {
        atTopOfPage: true
      }
    }
  },
// a beforeMount call to add a listener to the window
  beforeMount () {
    window.addEventListener('scroll', this.handleScroll);
  },
  methods: {
    // the function to call when the user scrolls, added as a method
    handleScroll(){
      // when the user scrolls, check the pageYOffset
      if(window.pageYOffset>0){
        // user is scrolled
        if(this.view.atTopOfPage) this.view.atTopOfPage = false
      }else{
        // user is at top of page
        if(!this.view.atTopOfPage) this.view.atTopOfPage = true
      }
    },
    toggleMenu() {
      this.isOpen = !this.isOpen;
    }
  }
}
</script>

<style scoped lang="scss">
nav {
  z-index: 10
}

nav.scrolled {
  @apply shadow-2xl;
  border-bottom: 0px;
}

.dropdown-title:hover {
  .dropdown-menu {
    display: block;
  }
}
</style>

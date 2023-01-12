<template>
  <nav class="
      container
      mx-auto px-8
      py-4
      lg:flex lg:justify-between lg:items-center md:px-10
    ">
    <div class="flex items-center justify-between">
      <router-link to="/">
        <p class="text-white font-outfit font-bold text-xl md:text-2xl">Homex.</p>
      </router-link>
      <!-- Mobile menu button -->
      <div>
        <button aria-label="menu" type="button" @click="showMenu = !showMenu" class="
          flex lg:hidden
            text-white
            hover:text-gray-400
            focus:outline-none focus:text-gray-400
          ">
          <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
            <path fill-rule="evenodd"
            d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0
            6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z">
            </path>
          </svg>
        </button>
      </div>
    </div>

    <!-- Mobile Menu open: "block", Menu closed: "hidden" -->
    <ul :class="showMenu ? 'flex' : 'hidden'" class="
        flex-col
        mt-8
        space-y-4
        lg:flex
        lg:space-y-0
        lg:flex-row
        lg:items-center
        lg:space-x-12
        lg:mt-0
      ">
      <ListMenu menu="Home"/>
      <ListMenu menu="About"/>
      <ListMenu menu="Services"/>
      <ListMenu menu="Contact"/>
      <button aria-label="lets talk" class="text-[#151D48] font-poppins bg-white hover:bg-gray-200
      focus:ring-4 focus:outline-none focus:ring-blue-300
      font-medium rounded-lg text-sm px-5 py-2 text-center
      mr-2 block lg:hidden">
        Lets Talk
      </button>
    </ul>
    <div>
      <router-link to="/">
      <button aria-label="lets talk" class="text-[#151D48] font-poppins bg-white hover:bg-gray-200
      focus:ring-4 focus:outline-none focus:ring-blue-300
      font-medium rounded-lg text-sm px-5 py-2 text-center
      mr-2 hidden lg:block">
        Lets Talk
      </button>
      </router-link>
    </div>
  </nav>
</template>

<script setup>
import ListMenu from '@/components/Navbar/ListMenu/index.vue';
import { ref } from 'vue';

const showMenu = ref(false);
</script>

<script>
export default {
  name: 'NavigationBar',
};
</script>

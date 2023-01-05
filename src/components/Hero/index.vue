<template>
  <section class="text-center container flex mx-auto px-8 space-x-0 md:space-x-28
  lg:space-x-38 md:flex md:justify-between md:items-center md:text-left md:px-10">
    <div class="my-8">
      <h1 class="text-xl font-poppins font-semibold text-white
      tracking-wide md:text-4xl lg:text-6xl">
        Discover Most Suitable
      </h1>
      <h1 class="text-[#567AE5] text-xl font-poppins font-semibold
      tracking-wide md:text-4xl lg:text-6xl">
        Property
      </h1>
      <p class="text-xs font-outfit text-white mt-2 tracking-wide md:text-sm md:mt-5 lg:mt-8">
        Non id ut volutpat urna, nulla ornare tempus molestie tincidunt.
        A vitae ut purus non elementum sapien ac at.
      </p>
      <form>
        <div class="relative my-5 md:mt-8">
          <div class="absolute inset-y-0 left-0 flex items-center pl-3 pointer-events-none">
            <svg aria-hidden="true" class="w-5 h-5 text-gray-500 dark:text-gray-400" fill="none"
              stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
            </svg>
          </div>
          <label for="search">
            <input type="search" id="search"
            class="block w-full p-2 pl-10 text-xs text-gray-900 font-outfit border
                border-gray-300 rounded-lg bg-gray-50 focus:ring-blue-500 focus:border-blue-500
                md:p-4 md:pl-10 md:text-sm"
              placeholder="Search by Location" required>
          </label>
          <button type="submit"
          class="text-white font-outfit absolute right-1.5 bottom-1.5 bg-blue-700 hover:bg-blue-800
              focus:ring-4 focus:outline-none focus:ring-blue-300
              rounded-lg text-xs px-2 py-1 md:py-2 md:right-2.5 md:bottom-2.5 md:text-sm md:px-4">
            Search
          </button>
        </div>
      </form>
    </div>
    <div class="row">
      <img src="image.png"
      alt="image"
      class="lg:max-w-2xl h-full w-full my-10 inset-y-0 right-0 hidden md:block">
    </div>
  </section>
</template>

<script>
export default {
  name: 'HeroSection',
};
</script>

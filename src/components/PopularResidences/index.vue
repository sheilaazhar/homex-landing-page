<template>
<section>
  <div class="text-center">
    <h2 class="text-xl font-poppins font-semibold mt-14 md:text-3xl md:mt-28">
      Popular Residences
    </h2>
    <p class="text-xs font-outfit text-gray-600 mt-2 leading-5 md:text-sm md:mt-5">
      Integer dictum urna, mauris imperdiet. Sollicitudin enim vitae laoreet lorem quis eget.
      Nam potenti dolor dui, netus.
    </p>
  </div>
  <div
  class="grid grid-cols-1 gap-4 place-items-center mt-5 md:grid-cols-2 lg:grid-cols-3 md:mt-10">
    <div v-for="residence in residences" :key="residence.id">
      <div class="w-full max-w-xs bg-[#F9FAFB] border rounded-xl shadow-md md:max-w-sm">
        <a href="#">
          <img class="rounded-xl p-5"
          :src="residence.image" alt="image" />
        </a>
        <div class="px-5 pb-5">
          <a href="#">
            <h5 class="text-lg font-poppins font-semibold tracking-tight text-gray-900 md:text-xl">
              {{ residence.name }}</h5>
          </a>
          <p class="text-xs font-poppins mt-2 text-[#737791] md:text-sm">
            {{ residence.description }}
          </p>
          <div class="flex items-center justify-between">
            <span class="text-lg font-poppins font-semibold mt-2 text-[#567AE5] md:text-xl">
              ${{ residence.price }}
            </span>
            <a href="#"
              class="text-white bg-[#567AE5] hover:bg-blue-800 focus:ring-4
              focus:outline-none focus:ring-blue-300 font-poppins font-medium rounded-lg text-xs
              px-3 py-1.5 text-center md:px-5 md:py-1.5 md:text-sm">Book Now</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
</template>

<script>
export default {
  name: 'PopularResidences',
  data() {
    return {
      residences: [
        {
          id: 1,
          name: 'Varius odio vel',
          description: 'Sagittis, odio turpis amet at lacinia ornare id. Felis bibendum.',
          price: '25,253',
          image: 'residence1.png',
        },
        {
          id: 2,
          name: 'Blandit volutpat nunc',
          description: 'Suspendisse pellentesque vestibulum tincidunt in diam libero dolor urna',
          price: '25,253',
          image: 'residence2.png',
        },
        {
          id: 3,
          name: 'Eu tempus, gravida',
          description: 'Rhoncus pellentesque et porttitor mi adipiscing vitae odio enim',
          price: '25,253',
          image: 'residence3.png',
        },
      ],
    };
  },
};
</script>

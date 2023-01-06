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
    <swiper :initial-slide="1" :slides-per-view="1" :spaceBetween="5" :loop="true" :pagination="{
      clickable: true,
    }" :centered-slides="true" :centered-slides-bounds="true" :grabCursor="true" :modules="modules"
      :breakpoints="swiperBreakpoints" class="mySwiper grid grid-cols-3 gap-2 place-items-center">
      <swiper-slide v-for="residence in residences" :key="residence.id">
        <div class="w-full max-w-xs bg-[#F9FAFB] border rounded-xl shadow-md md:max-w-sm">
          <router-link to="/">
            <img class="rounded-xl p-5" :src="residence.image" alt="image" />
          </router-link>
          <div class="px-5 pb-5">
            <router-link to="/">
              <h5 class="text-lg font-poppins font-semibold tracking-tight
              text-gray-900 md:text-xl">
                {{ residence.name }}</h5>
            </router-link>
            <p class="text-xs font-poppins mt-2 text-[#737791] md:text-sm">
              {{ residence.description }}
            </p>
            <div class="flex items-center justify-between">
              <span class="text-lg font-poppins font-semibold mt-2 text-[#567AE5] md:text-xl">
                ${{ residence.price }}
              </span>
              <router-link to="/">
                <button class="text-white bg-[#567AE5] hover:bg-blue-800 focus:ring-4
              focus:outline-none focus:ring-blue-300 font-poppins font-medium rounded-lg text-xs
              px-3 py-1.5 text-center md:px-5 md:py-1.5 md:text-sm">Book Now</button>
              </router-link>
            </div>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </section>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Pagination, Navigation } from 'swiper';
// eslint-disable-next-line import/extensions
import 'swiper/css';
// eslint-disable-next-line import/extensions
import 'swiper/css/navigation';
// eslint-disable-next-line import/extensions
import 'swiper/css/pagination';

export default {
  name: 'PopularResidences',
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination, Navigation],
    };
  },
  data() {
    return {
      swiperBreakpoints: {
        768: {
          slidesPerView: '2',
        },
        1280: {
          slidesPerView: '3',
        },
      },
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

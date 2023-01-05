<template>
<section>
  <div class="text-center">
    <h2 class="text-xl font-poppins font-semibold mt-24 md:text-3xl md:mt-36">
      What Our Customer Say About Us
    </h2>
    <p class="text-xs text-[#737791] font-outfit mt-3 mb-8 leading-5 md:text-sm md:mt-5">
      Arcu, accumsan quam mi porttitor etiam in. Libero egestas <br> amet, quam sagittis.
    </p>
  </div>
  <div class="flex flex-wrap -mx-1 lg:-mx-4">
  <!-- Column -->
  <div class="my-5 px-1 w-full md:w-1/2 lg:my-1 lg:px-4 lg:w-1/3 md:my-4"
  v-for="review in reviews" :key="review.id">
    <div class="max-w-sm w-full lg:max-w-full lg:flex relative">
      <img src="review.png" alt="review" class="w-10 h-10 absolute top-[-25px] left-[20px]" />
      <div
      class="border border-gray-200 bg-gray-100 rounded-lg p-4 flex flex-col
      justify-between leading-normal">
        <div class="mb-5">
          <p class="text-[#70798B] text-base font-poppins">
            {{ review.content }}</p>
        </div>
        <div class="flex items-center">
          <img class="w-10 h-10 rounded-full mr-4"
          :src="review.image"
          alt="Avatar of Jonathan Reinink">
          <div class="text-sm">
            <p class="text-[#151D48] leading-none font-semibold font-poppins">{{ review.name }}</p>
            <p class="text-[#737791] leading-none mt-1 font-poppins">{{ review.job }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
  </div>
  <GetStarted/>
</section>
</template>

<script>
import GetStarted from '@/components/CustomerSay/GetStarted/index.vue';

export default {
  name: 'CustomerSay',
  components: {
    GetStarted,
  },
  data() {
    return {
      reviews: [
        {
          id: 1,
          name: 'Adalberto Kovach',
          content: 'There are many variations of passages of Lorem Ipsum form, by injected humour randomised words.',
          job: 'Marketing Management',
          image: 'person1.png',
        },
        {
          id: 2,
          name: 'Gino Lavender',
          content: 'There are many variations of passages of Lorem Ipsum form, by injected humour randomised words.',
          job: 'Marketing Management',
          image: 'person2.png',
        },
        {
          id: 3,
          name: 'Pedro Pounds',
          content: 'There are many variations of passages of Lorem Ipsum form, by injected humour randomised words.',
          job: 'Marketing Management',
          image: 'person3.png',
        },
      ],
    };
  },
};
</script>

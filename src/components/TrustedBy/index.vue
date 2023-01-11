<template>
<section class="text-center">
  <h2 class="text-xl font-poppins font-semibold mt-10 md:text-3xl md:mt-20">TrustedBy</h2>
  <p class="text-xs font-outfit text-gray-600 mt-2 leading-5 md:text-sm md:mt-5">
    Non egestas nunc tempor pellentesque consequat. <br> Metus neque, sodales nisl mauris.
  </p>
  <div class="grid grid-cols-3 gap-6 place-items-center mt-5 md:mt-10 lg:gap-4 md:grid-cols-5">
    <div v-for="company in companies" :key="company.id">
      <img :src="company.image" :alt="company.desc" width="129" height="47" loading="lazy">
    </div>
  </div>
</section>
</template>

<script>
export default {
  name: 'TrustedBy',
  data() {
    return {
      companies: [
        {
          id: 1,
          image: 'ifttt.png',
          desc: 'IFTTT Logo',
        },
        {
          id: 2,
          image: 'amazon.png',
          desc: 'Amazon Logo',
        },
        {
          id: 3,
          image: 'google.png',
          desc: 'Google Logo',
        },
        {
          id: 4,
          image: 'paypal.png',
          desc: 'Paypal Logo',
        },
        {
          id: 5,
          image: 'airbnb.png',
          desc: 'Airbnb Logo',
        },
      ],
    };
  },
};
</script>

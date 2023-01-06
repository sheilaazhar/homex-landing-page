<template>
  <section class="grid grid-cols-1 gap-4 place-items-center text-center mt-20
  lg:grid-cols-2 lg:place-items-start lg:mt-28 lg:text-left">
    <div>
      <img class="max-w-xs lg:max-w-md px-10 sm:p-0" src="house.png" alt="house image" />
    </div>
    <div>
      <h2 class="text-xl font-poppins font-semibold mt-5 md:text-3xl md:mt-30">
        Comfort is Our Top Priority for you
      </h2>
      <p class="text-xs font-outfit text-[#737791] mt-2 md:text-sm md:mt-3">
        Congue enim vitae a ultricies feugiat aliquet netus leo. Nec, volutpat volutpat
        vulputate adipiscing.
      </p>
      <ul class="list-disc marker:text-[#567AE5] list-inside pl-5 mt-2 text-sm font-outfit">
        <li>Premium National Marketing</li>
        <li>Free, no Obligation Valuations</li>
      </ul>
      <router-link to="/">
        <button class="text-white bg-[#567AE5] hover:bg-blue-800 focus:ring-4
              focus:outline-none focus:ring-blue-300 font-medium rounded-lg
              text-sm px-3 py-1.5 text-center font-poppins mt-3 md:px-5 md:py-2">
          See More
        </button>
      </router-link>
    </div>
  </section>
</template>

<script>
export default {
  name: 'TopPriority',
};
</script>

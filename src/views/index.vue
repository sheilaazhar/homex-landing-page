<template>
<header class="bg-[#151D48] min-h-[47px] md:min-h-[93px]">
  <NavigationBar/>
  <HeroSection/>
</header>

<main class="bg-white container mx-auto px-8 md:px-10">
  <TrustedBy/>
  <PopularResidences/>
  <TopPriority/>
  <CustomerSay/>
</main>

<FooterBar/>
</template>

<script>
import NavigationBar from '@/components/Navbar/index.vue';
import HeroSection from '@/components/Hero/index.vue';
import TrustedBy from '@/components/TrustedBy/index.vue';
import PopularResidences from '@/components/PopularResidences/index.vue';
import TopPriority from '@/components/TopPriority/index.vue';
import CustomerSay from '@/components/CustomerSay/index.vue';
import FooterBar from '@/components/Footer/index.vue';

export default {
  name: 'LandingPage',
  components: {
    NavigationBar,
    HeroSection,
    TrustedBy,
    PopularResidences,
    TopPriority,
    CustomerSay,
    FooterBar,
  },
};
</script>

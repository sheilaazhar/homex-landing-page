<template>
  <router-link to="/"
  class="text-md font-medium font-outfit text-white hover:text-blue-400 cursor-pointer">
    {{ menu }}
  </router-link>
</template>

<script setup>
defineProps({
  menu: String,
});
</script>

<script>
export default {
  name: 'ListMenu',
};
</script>

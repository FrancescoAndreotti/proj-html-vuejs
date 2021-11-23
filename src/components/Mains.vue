<template>
  <div>
    <AboutTheCompany></AboutTheCompany>
    <Services></Services>
    <Pricing></Pricing>
  </div>
</template>

<script>
import AboutTheCompany from "./AboutTheCompany.vue";
import Services from "./Services.vue";
import Pricing from "./Pricing.vue";
export default {
  components: {
    AboutTheCompany,
    Services,
    Pricing,
  },
};
</script>

<style scoped>
</style>

<template>
  <div>
    <AboutTheCompany></AboutTheCompany>
    <Services></Services>
    <Pricing></Pricing>
    <News></News>
    <Newsletter></Newsletter>
    <Form></Form>
  </div>
</template>

<script>
import AboutTheCompany from "./AboutTheCompany.vue";
import Services from "./Services.vue";
import Pricing from "./Pricing.vue";
import Newsletter from "./Newsletter.vue";
import News from "./News.vue";
import Form from "./Form.vue";
export default {
  components: {
    AboutTheCompany,
    Services,
    Pricing,
    Newsletter,
    News,
    Form,
  },
};
</script>

<style scoped>
</style>

<template>
  <div>
    <div class="container-fluid">
      <div class="container">
        <div class="row">
          <div class="col-8 offset-2 text-center">
            <h6 class="mb-4">Monthly plans</h6>
            <h2><span>Pricing</span>Table</h2>
            <p>
              We can help you deliver and execute your future, wherever you
              compete, using the latest thechnologies, from strategy development
              to implementation
            </p>
          </div>
        </div>
        <div class="row row-cols-3">
          <div class="col" v-for="(card, i) in cards" :key="i">
            <div class="card">
              <span v-if="card.title === `Professional`">Most Popular</span>
              <i :class="card.icon"></i>
              <h3>{{ card.title }}</h3>
              <span>{{ card.price }}</span>
              <ul>
                <li v-for="(future, e) in card.futures" :key="e">
                  {{ future.future }}
                  <i :class="future.value ? `fa fa-check` : `fa fa-times`"></i>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          icon: "fa fa-rocket",
          title: "Standard",
          price: "$490 /mo",
          futures: [
            {
              future: "Standard Accounting",
              value: true,
            },
            {
              future: "Platform Acces",
              value: true,
            },
            {
              future: "Business Orientation",
              value: false,
            },
            {
              future: "Dedicated Consultant",
              value: false,
            },
            {
              future: "Personal Assistance",
              value: false,
            },
          ],
        },
        {
          icon: "fa fa-briefcase",
          title: "Professional",
          price: "$890 /mo",
          futures: [
            {
              future: "Standard Accounting",
              value: true,
            },
            {
              future: "Platform Acces",
              value: true,
            },
            {
              future: "Business Orientation",
              value: true,
            },
            {
              future: "Dedicated Consultant",
              value: false,
            },
            {
              future: "Personal Assistance",
              value: false,
            },
          ],
        },
        {
          icon: "fa fa-diamond",
          title: "Ultimate",
          price: "$1.390 /mo",
          futures: [
            {
              future: "Standard Accounting",
              value: true,
            },
            {
              future: "Platform Acces",
              value: true,
            },
            {
              future: "Business Orientation",
              value: true,
            },
            {
              future: "Dedicated Consultant",
              value: true,
            },
            {
              future: "Personal Assistance",
              value: true,
            },
          ],
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../scss/app.scss";
.container-fluid {
  padding: 100px;
  background-color: #eef4ed;
}
h2 {
  font-weight: 900;
  font-size: 40px;
  margin-bottom: 30px;
  span {
    color: $primary-green;
    background-color: $secondary-green;
    padding: 0 10px;
  }
}
</style>
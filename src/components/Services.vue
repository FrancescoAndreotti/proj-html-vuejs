<template>
  <div>
    <div class="container-fluid">
      <div class="container">
        <div class="row">
          <div class="col">
            <h6>Our business areas</h6>
            <h2>Excellence in <span>Services</span></h2>
            <div class="row mb-5">
              <p class="col-10">
                We are leaders in providing consultancy services with a set of
                cutting-edge thechnologies and a team of experienced and renowed
                professionals. These are some options that you can hire.
              </p>
              <button class="my-btn-secondary col-1 offset-1">See all</button>
            </div>
            <div class="row row-cols-3 g-4">
              <div class="col" v-for="(card, i) in cards" :key="i">
                <div class="card">
                  <i :class="card.icon" class="mb-2"></i>
                  <h3 class="mb-3">{{ card.title }}</h3>
                  <p class="mb-3">{{ card.text }}</p>
                  <button class="my-btn-secondary">read more</button>
                </div>
              </div>
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
          icon: "fa fa-sitemap",
          title: "Audit & Assurance",
          text: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        {
          icon: "fa fa-briefcase",
          title: "Financial Advisory",
          text: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        {
          icon: "fa fa-bar-chart",
          title: "Analytics and M&A",
          text: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        {
          icon: "fa fa-plane",
          title: "Middle Marketing",
          text: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        {
          icon: "fa fa-globe",
          title: "Legal Consulting",
          text: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        {
          icon: "fa fa-archive",
          title: "Regulatory Risk",
          text: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../scss/app.scss";
.container-fluid {
  background-color: #111117;
  color: white;
  padding: 100px;

  h6 {
    color: $primary-green;
    font-size: 12px;
    margin-bottom: 15px;
  }
  h2 {
    font-weight: 900;
    font-size: 40px;
    margin-bottom: 30px;
    span {
      color: $primary-green;
      background-color: #0e272d;
    }
  }
  .card {
    background-color: #19191f;
    padding: 30px;
    border-radius: 10px;
    i {
      color: $primary-green;
      font-size: 30px;
    }

    .my-btn-secondary {
      max-width: 150px;
    }
  }
}
</style>
<template>
  <div>
    <div class="container">
      <div class="row mb-5">
        <div class="col">
          <h6>Our editorial content</h6>
          <h2>Latest <span>News</span></h2>
          <div class="d-flex justify-content-between align-items-center">
            <p>
              Every week we publish content about is best in the business world
            </p>
            <button class="my-btn-primary">See all</button>
          </div>
        </div>
      </div>
      <div class="row row-cols-3">
        <div class="col" v-for="(card, i) in cards" :key="i">
          <div class="card position-relative">
            <img :src="card.img" alt="" />
            <p class="text-center">{{ card.text }}</p>
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
          img: require("@/assets/img/news-1.jpg"),
          text: "Increaing creativity is possible for everyone",
        },
        {
          img: require("@/assets/img/news-2.jpg"),
          text: "Because market research is part of the business plan",
        },
        {
          img: require("@/assets/img/news-3.jpg"),
          text: "Working from home is now a trend",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../scss/app.scss";

.container {
  padding: 100px 0;
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

.card {
  border-radius: 15px;
  overflow: hidden;
  transition: transform 1s;
  &:hover {
    transform: translateY(-10px);
  }
  p {
    position: absolute;
    bottom: 25px;
    left: 25px;
    right: 25px;
    color: white;
    font-size: 25px;
    font-weight: bold;
  }
}
</style>
<template>
  <div>
    <div class="container-fluid cards-container">
      <div class="container">
        <div class="row row-cols-3">
          <div class="col" v-for="(card, i) in cards" :key="i">
            <div class="card">
              <i :class="card.icon"></i>
              <h2>{{ card.title }}</h2>
              <p>{{ card.text }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container-fluid position-relative">
      <div class="container">
        <div class="row row-col-2">
          <div class="img-container">
            <img src="../assets/img/about-3.jpg" alt="" class="img-fluid" />
          </div>
          <div class="col about">
            <div class="my-5">
              <h6 class="text-uppercase">about the network</h6>
              <h2><span>The</span> Company</h2>
              <p>
                For 12 years we have been providing audit and warranty,
                financial advice, risk advice, taxes and related services to
                select clients.
              </p>
            </div>
            <div class="row row-cols-2 the-company">
              <div class="col">
                <i class="fa fa-bitbucket" aria-hidden="true"></i>
                <span>Tradition</span>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
              </div>
              <div class="col">
                <i class="fa fa-lock" aria-hidden="true"></i>
                <span>Security</span>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
              </div>
              <div class="col">
                <i class="fa fa-pencil-square-o" aria-hidden="true"></i>
                <span>Certificate</span>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
              </div>
              <div class="col">
                <i class="fa fa-graduation-cap" aria-hidden="true"></i>
                <span>Expertise</span>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
              </div>
            </div>
          </div>
          <div class="col"></div>
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
          icon: "fa fa-users",
          title: "Human Capital",
          text: "Humanizing business: Harness the power of thechnology to improve the way people work.",
        },
        {
          icon: "fa fa-pie-chart",
          title: "Core Business",
          text: "It taken innovative approaches to trasform, modernize, and run existing platform.",
        },
        {
          icon: "fa fa-tachometer",
          title: "Performace",
          text: "Achieve maximum impact and value from investments in finance and supply chain.",
        },
      ],
    };
  },
};
</script>


<style scoped lang="scss">
@import "../scss/app.scss";

.cards-container {
  background-color: #eef4ed;
  padding: 80px;

  .card {
    padding: 30px;
    transition: transform 1s;
    &:hover {
      transform: translateY(-10px);
    }

    h2 {
      margin-bottom: 20px;
    }
    i {
      color: #038483;
      background-color: $secondary-green;
      font-size: 20px;
      padding: 15px;
      border-radius: 50%;
      height: 50px;
      width: 50px;
      margin-bottom: 20px;
    }
  }
}
.img-container {
  position: absolute;
  top: 0;
  left: 50%;
  right: 0;
  bottom: 0;
  width: 50%;
  overflow: hidden;
}

.about {
  padding-top: 40px;
  padding-bottom: 40px;
  padding-right: 40px;

  h6 {
    color: $primary-green;
    font-size: 12px;
    margin-bottom: 30px;
  }
  h2 {
    font-weight: 900;
    font-size: 40px;
    margin-bottom: 30px;
    span {
      color: $primary-green;
      background-color: $secondary-green;
      padding: 5px;
    }
  }
  .the-company {
    i {
      color: $primary-green;
      padding: 5px;
      margin-bottom: 15px;
    }
    span {
      font-size: 20px;
      font-weight: bold;
      margin-bottom: 15px;
    }
    .col {
      margin-bottom: 30px;
    }
  }
}
</style>
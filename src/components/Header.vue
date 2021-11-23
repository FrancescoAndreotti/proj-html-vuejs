<template>
  <div class="root">
    <!-- NAV Informaioni -->
    <div class="container-fluid contacts">
      <div class="container d-flex justify-content-between">
        <div>
          <span class=""
            ><i class="fa fa-clock-o"></i> Open Hours: Mon - Sat - 9:00 -
            18:00</span
          >
        </div>
        <div>
          <span>
            <i class="fa fa-phone" aria-hidden="true"></i>
            +1(305 1234-5678)
          </span>
          <span>
            <i class="fa fa-envelope" aria-hidden="true"></i>
            Hello@example.com
          </span>
          <span>
            <i class="fa fa-facebook mx-3" aria-hidden="true"></i>
            <i class="fa fa-twitter mx-3" aria-hidden="true"></i>
            <i class="fa fa-linkedin mx-3" aria-hidden="true"></i>
          </span>
        </div>
      </div>
    </div>
    <!-- Fine NAV -->

    <div class="container-fluid hero">
      <div class="container">
        <nav class="d-flex justify-content-between">
          <div class="text-uppercase fw-bold text-white nex">
            <span>nex</span>gen
          </div>
          <div>
            <!-- Link -->
            <ul class="nav d-flex align-items-center">
              <li class="nav-item" v-for="(item, i) in linkNav" :key="i">
                <a class="text-uppercase fw-bolder" :href="item.link">{{
                  item.text
                }}</a>
              </li>
              <button class="my-btn-primary">Get in touch</button>
            </ul>

            <!-- fine link -->
          </div>
        </nav>
        <div class="text-center">
          <h1>Lead ~ Customer</h1>
          <p>
            Succesful strategies require data analysis, creativity and customer
            focus, taking advantage of the latest technologies to offer
            excellent services.
          </p>
          <button class="my-btn-primary mx-3">Get in touch</button>
          <button class="my-btn-secondary">read more</button>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  data() {
    return {
      linkNav: [
        {
          link: "/home",
          text: "home",
        },
        {
          link: "/about",
          text: "about",
        },
        {
          link: "/services",
          text: "services",
        },
        {
          link: "/pricing",
          text: "pricing",
        },
        {
          link: "/blog",
          text: "blog",
        },
      ],
    };
  },
};
</script>


<style lang="scss" scoped>
/* Nav Informazioni */

.contacts {
  background-color: #21333e;
  color: #b7c1c2;
  padding: 10px;

  span {
    margin: 0 15px;
  }
}

/* Fine Nav Informazioni */

.hero {
  background-image: url("../assets/img/hero-image.png");
  background-size: cover;
  position: relative;
  &::after {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba($color: #000000, $alpha: 0.5);
  }
  .nex {
    letter-spacing: 3px;
    font-size: 20px;

    span {
      color: #038483;
      background-color: #03848431;
      border-radius: 15px 0 0 15px;
      padding-left: 15px;
      padding-top: 6px;
      padding-bottom: 6px;
    }
  }
  .container {
    z-index: 99;
    position: relative;

    .text-center {
      padding: 200px;

      h1 {
        font-weight: 800;
        font-size: 60px;
        color: white;
        margin-bottom: 20px;
      }

      p {
        color: #bfc7ca;
        margin-bottom: 30px;
      }
    }
  }
  nav {
    padding: 25px;
    a {
      text-decoration: none;
      color: rgb(255, 255, 255);
      padding: 20px;
    }
  }
}
</style>
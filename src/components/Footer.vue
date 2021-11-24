<template>
  <div>
    <div class="container-fluid big-bg">
      <div class="container">
        <div class="row row-cols-4">
          <div class="col">
            <div class="text-uppercase fw-bold text-white nex mb-3">
              <span>nex</span>gen
            </div>
            <p class="mb-3">
              A functional HTML Template for Corporate & Business
            </p>
            <div class="mb-2">
              <i class="fa fa-phone" aria-hidden="true"></i>
              <span> +1 (305) 1234-5678</span>
            </div>
            <div class="mb-2">
              <i class="fa fa-envelope" aria-hidden="true"></i>
              <span> Hello@example.com</span>
            </div>
            <div class="mb-2">
              <i class="fa fa-map-marker" aria-hidden="true"></i>
              <span> Main Avenue, 987</span>
            </div>
            <div><button class="my-btn-secondary">Get in touch</button></div>
          </div>

          <!-- Cards -->
          <div class="col" v-for="(card, i) in cards" :key="i">
            <div class="card">
              <h3>{{ card.title }}</h3>
              <ul>
                <li v-for="(li, k) in card.li" :key="k">
                  <a href="#"
                    ><i class="fa fa-angle-right" aria-hidden="true"></i>
                    {{ li }}</a
                  >
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container-fluid small-bg">
      <div class="container">
        <div class="row">
          <div class="col">
            <p>Enjoy the low price. We are traking any intention of piracy.</p>
          </div>
          <div class="col text-end">
            <p>©2020 NEXGEN is Proudly Powered by <span>Codings</span></p>
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
          title: "About",
          li: [
            "The Company",
            "Institutional",
            "Social & Event",
            "Innovataion",
            "Enviroment",
            "Technology",
          ],
        },
        {
          title: "Services",
          li: [
            "Audit & Assurance",
            "Financial Advisory",
            "Analytics M&A ",
            "Middle Marketing",
            "Legal Consulting",
            "Regulatory Risk",
          ],
        },
        {
          title: "Support",
          li: [
            "Responsibilty",
            "Term of Use",
            "About Cookies",
            "Privacy Policy",
            "Accessibility",
            "Information",
          ],
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
.big-bg {
  background-color: #111117;
  color: rgb(150, 148, 148);
  padding: 100px;

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

  .card {
    background-color: #19191f;
    padding: 30px;
    display: flex;
    justify-content: space-between;
    max-width: 250px;
    border-radius: 15px;

    ul {
      list-style-type: none;
      padding: 0;
      a {
        text-decoration: none;
        color: rgb(150, 148, 148);
        &:hover {
          font-size: 20px;
        }
      }
    }
    h3 {
      color: white;
    }
  }
}

.small-bg {
  background-color: #0d0d11;
  color: rgb(150, 148, 148);

  span {
    color: #038483;
  }
}
</style>
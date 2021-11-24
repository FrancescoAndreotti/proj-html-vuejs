<template>
  <div>
    <div class="newsletter-container">
      <div class="row justify-content-center">
        <div class="col">
          <h6>newsletter</h6>
          <h2><span>Know</span> First</h2>
          <p>
            Follow closely and receive content about our company and the news of
            the current market.
          </p>
        </div>
        <div class="col d-flex flex-column">
          <input type="text" placeholder="Name" />
          <input type="email" placeholder="Email" />
          <button class="my-btn-primary">Subscribe</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
@import "../scss/app.scss";

.newsletter-container {
  background-image: url("../assets/img/bg-1.jpg");
  padding: 100px 200px;
  background-position: center;

  button {
    width: 120px;
  }
  h2 {
    color: white;
    margin-bottom: 30px;

    span {
      background-color: #0384844f;
      font-weight: bold;
    }
  }

  p {
    color: rgb(150, 148, 148);
  }

  input {
    background-color: #ffffffb6;
    border: none;
    padding: 5px;
    width: 400px;
    height: 40px;
    margin-bottom: 20px;
    border-radius: 5px;
  }
}
</style>
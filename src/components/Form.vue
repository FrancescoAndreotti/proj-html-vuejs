<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="col-8">
          <h6>Send a message</h6>
          <h2>Get in <span>Touch</span></h2>
          <p>We will respond to your message as soon as possible.</p>
          <div>
            <input type="text" placeholder="Name" />
            <input type="email" placeholder="Email" />
          </div>
          <div>
            <input type="number" placeholder="Phone" />
            <input type="text" placeholder="More info" />
          </div>
          <div><input type="text" placeholder="Message" class="message" /></div>
          <div><button class="my-btn-primary">send</button></div>
        </div>

        <!-- left col -->
        <div class="col-4">
          <h4>Example Inc.</h4>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
          <p>Praesent diam lacus, dapibus sed imperdiet consectetur.</p>
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
          <div>
            <button class="my-btn-secondary my-special-btn">send</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
.container {
  padding: 100px;
}
h2 {
  font-weight: 900;
  font-size: 40px;
  margin-bottom: 30px;
  span {
    color: #038483;
    background-color: #daeced;
    padding: 0 10px;
  }
}
p {
  color: rgb(150, 148, 148);
}
input {
  background-color: #ececec;
  border: none;
  padding: 5px;
  width: calc(50% - 40px);
  height: 40px;
  margin-bottom: 20px;
  border-radius: 5px;
  margin-right: 20px;
}

.message {
  width: calc(100% - 60px);
  height: 100px;
}

i {
  color: #038483;
  background-color: #daeced;
  font-size: 20px;
  padding: 15px;
  border-radius: 50%;
  height: 50px;
  width: 50px;
  margin-bottom: 20px;
}
span {
  color: #038483;
}

.my-special-btn {
  color: #038483;
}
</style>
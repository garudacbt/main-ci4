<template>
    <div class="login" :style="{ backgroundImage: 'url(' + mainImageSrc + ')' }">
      <div class="container d-flex flex-column">
        <div class="row align-items-center justify-content-center g-0 min-vh-100">
          <div class="col-12 col-md-7 col-lg-5 col-xxl-4 py-8 py-xl-0">
            <!-- Card -->
            <div class="card smooth-shadow-md">
              <!-- Card body -->
              <div class="card-body p-6">
                <div class="mb-4">
                  <h4 class="mb-6 text-lg-center">L O G I N</h4>
                </div>
                <!-- Form -->
                <form>
                  <!-- Username -->
                  <div class="mb-3">
                    <label for="email" class="form-label">Username</label>
                    <input type="email" id="email" class="form-control" name="email" placeholder="Username" required="">
                  </div>
                  <!-- Password -->
                  <div class="mb-3">
                    <label for="password" class="form-label">Password</label>
                    <input type="password" id="password" class="form-control" name="password" placeholder="Password" required="">
                  </div>
                  <!-- Checkbox -->
                  <!--
                  <div class="d-lg-flex justify-content-between align-items-center mb-4">
                    <div class="form-check custom-checkbox">
                      <input type="checkbox" class="form-check-input" id="rememberme">
                      <label class="form-check-label" for="rememberme">Remember
                        me</label>
                    </div>
                  </div>
                  -->
                  <div>
                    <!-- Button -->
                    <div class="d-grid">
                      <button type="submit" class="btn btn-primary">Sign in</button>
                    </div>
                    <!--
                    <div class="d-md-flex justify-content-between mt-4">
                      <div class="mb-2 mb-md-0">
                        <a href="sign-up.html" class="fs-5">Create An Account </a>
                      </div>
                      <div>
                        <a href="forget-password.html" class="text-inherit
                        fs-5">Forgot your password?</a>
                      </div>
                    </div>
                    -->
                  </div>
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
  export default {
    name: 'Login',

    components: {},

    mixins: [],

    props: {},

    data() {
      return {
        images: [],
        mainImageSrc: null
      }
    },

    computed: {},

    watch: {},

    created() {
      let self = this;
      this.images = [
        {
          id: '1',
          image: require('@/assets/images/slide-img/slider-img-1.jpg')
        },
        {
          id: '2',
          image: require('@/assets/images/slide-img/slider-img-2.jpg')
        },
        {
          id: '3',
          image: require('@/assets/images/slide-img/slider-img-3.jpg')
        },
      ];

      setInterval(function () {
        self.mainImageSrc = self.images[Math.floor(Math.random() * self.images.length)].image;
      }, 5000);

    },
    methods: {},

  }
</script>

<style>

</style>

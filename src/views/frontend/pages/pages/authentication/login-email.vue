<template>
  <div class="login-body">
    <div class="main-wrapper">
      <layoutheader></layoutheader>

      <!-- Page Content -->
      <div class="login-content-info">
        <div class="container">
          <!-- Login Email -->
          <div class="row justify-content-center">
            <div class="col-lg-4 col-md-6">
              <div class="account-content">
                <div class="login-shapes">
                  <div class="shape-img-left">
                    <img src="@/assets/img/shape-01.png" alt="shape-image" />
                  </div>
                  <div class="shape-img-right">
                    <img src="@/assets/img/shape-02.png" alt="shape-image" />
                  </div>
                </div>
                <div class="account-info">
                  <div class="login-back">
                    <router-link to="/"
                      ><i class="fas fa-arrow-left-long"></i> Back</router-link
                    >
                  </div>
                  <div class="login-title">
                    <h3>Sign in</h3>
                    <p>We'll send a confirmation code to your email.</p>
                    <span
                      >Sign in with
                      <router-link to="/login-phone">Phone Number</router-link></span
                    >
                  </div>
                  <form action="/login-email-otp">
                    <div class="mb-3">
                      <label class="mb-2">E-mail</label>
                      <input
                        type="text"
                        class="form-control"
                        placeholder="example@email.com"
                      />
                    </div>
                    <div class="mb-3">
                      <div class="form-group-flex">
                        <label class="mb-2">Password</label>
                        <router-link to="/forgot-password" class="forgot-link"
                          >Forgot password?</router-link
                        >
                      </div>
                      <div class="pass-group">
                        <input
                          v-if="showPassword"
                          type="text"
                          class="form-control pass-input"
                          v-model="password"
                          placeholder="**********"
                        />
                        <input
                          v-else
                          type="password"
                          class="form-control pass-input"
                          placeholder="**********"
                          v-model="password"
                        />
                        <span
                          class="toggle-password"
                          @click="toggleShow"
                          :class="{
                            'feather-eye': showPassword,
                            'feather-eye-off': !showPassword,
                          }"
                        ></span>
                      </div>
                    </div>
                    <div class="mb-3 form-check-box">
                      <div class="form-group-flex">
                        <label class="custom_check d-inline-flex">
                          Remember Me
                          <input type="checkbox" name="login" />
                          <span class="checkmark"></span>
                        </label>
                        <label class="custom_check d-inline-flex">
                          Login with OTP
                          <input type="checkbox" name="login" />
                          <span class="checkmark"></span>
                        </label>
                      </div>
                    </div>
                    <div class="mb-3">
                      <b-button class="btn w-100" type="submit">Sign in</b-button>
                    </div>
                    <div class="login-or">
                      <span class="or-line"></span>
                      <span class="span-or">or</span>
                    </div>
                    <div class="social-login-btn">
                      <a href="javascript:void(0);" class="btn w-100">
                        <img src="@/assets/img/icons/google-icon.svg" alt="google-icon" />
                        Log in with Google
                      </a>
                    </div>
                    <div class="account-signup">
                      <p>
                        Don't have an account ?
                        <router-link to="/signup">Sign up</router-link>
                      </p>
                    </div>
                  </form>
                </div>
              </div>
            </div>
          </div>
          <!-- /Login Email -->
        </div>
      </div>
      <!-- /Page Content -->

      <cursor></cursor>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      showPassword: false,
      password: null,
    };
  },
  computed: {
    buttonLabel() {
      return this.showPassword ? "Hide" : "Show";
    },
  },
  methods: {
    toggleShow() {
      this.showPassword = !this.showPassword;
    },
  },
};
</script>

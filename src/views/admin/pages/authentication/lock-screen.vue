<template>
  <!-- Main Wrapper -->
  <div class="main-wrapper login-body">
    <div class="login-wrapper">
      <div class="container">
        <div class="loginbox">
          <div class="login-left">
            <img class="img-fluid" src="@/assets/admin/img/logo.png" alt="Logo" />
          </div>
          <div class="login-right">
            <div class="login-right-wrap">
              <div class="lock-user">
                <img
                  class="rounded-circle"
                  src="@/assets/admin/img/profiles/avatar-02.jpg"
                  alt="User Image"
                />
                <h4>John Doe</h4>
              </div>

              <!-- Form -->
              <form action="/admin/index">
                <div class="form-group">
                  <input class="form-control" type="text" placeholder="Password" />
                </div>
                <div class="form-group mb-0">
                  <b-button class="btn btn-primary w-100" type="submit">Enter</b-button>
                </div>
              </form>
              <!-- /Form -->

              <div class="text-center dont-have">
                Sign in as a different user?
                <router-link to="/admin/login">Login</router-link>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <!-- /Main Wrapper -->
</template>

<script>
export default {
  data() {
    return {};
  },
  name: "/admin/lock-screen",
};
</script>

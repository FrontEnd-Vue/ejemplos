<template>
  <div class="container">
    <div class="row">
      <div class="col-md-6">
        <div class="card">
          <div class="card-body">
            <div v-if="isLoggedIn">
              <p class="h3 fw-bold text-success">Welcome User</p>
              <p class="fst-italic">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ad hic impedit modi nulla
                placeat quas quo
                reprehenderit. Architecto corporis cupiditate eaque enim et perspiciatis quasi ut veritatis. Dolores,
                quo unde?</p>
            </div>
            <div v-if="!isLoggedIn">
              <p class="h3 fw-bold text-danger">Thank You!!</p>
              <p class="fst-italic">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aspernatur blanditiis
                consequatur dolore dolorum, eum expedita explicabo illo, iure iusto molestias nisi perferendis
                praesentium quae, quidem quod repellat reprehenderit sint totam.</p>
            </div>
            <div>
              <button v-if="!isLoggedIn" class="btn btn-success btn-sm m-1" @click="login()">Login</button>
              <button v-if="isLoggedIn" class="btn btn-danger btn-sm m-1" @click="logout()">LogOut</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AuthUser",
  data: function() {
    return {
      isLoggedIn: false
    };
  },
  methods: {
    login: function() {
      this.isLoggedIn = true;
    },
    logout: function() {
      this.isLoggedIn = false;
    }
  }
};
</script>

<style scoped>

</style>
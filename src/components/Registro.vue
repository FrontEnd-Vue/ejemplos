<template>
  <div class="container">
    <div class="row">
      <div class="col-md-3">
        <div class="card shadow-lg">
          <div class="card-header bg-success text-white">
            <p class="h3">Register Here</p>
          </div>
          <div class="card-body bg-light">
            <form @submit.prevent="register()">
              <div class="mb-2">
                <input v-model="user.name" 
                class="form-control" placeholder="Name" type="text">
              </div>
              <div class="mb-2">
                <input v-model="user.email"  class="form-control" placeholder="Email" type="email">
              </div>
              <div class="mb-2">
                <input v-model="user.password"  class="form-control" placeholder="Password" type="password">
              </div>
              <div class="mb-2">
                <input class="btn btn-success" type="submit" value="Register">
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "RegistroFrm",
  data: function() {
    return {
      user: {
        name: "",
        email: "",
        password: ""
      }
    };
  },
  methods: {
    validarCampo: function(value) {
      let valido = false
      if (value != '') {
        valido = true;
      }
      console.log('Entro...')
      return valido
    
    },
    register: function() {
      console.log(this.user);
    }
  }
};
</script>

<style scoped>

</style>
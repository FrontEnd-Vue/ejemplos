<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <p class="h3 fw-bold text-success">User List</p>
        <p class="fst-italic">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Expedita hic magni molestiae non
          sapiente soluta
          veniam voluptatem. Corporis debitis fuga illo minima natus necessitatibus qui reiciendis, repellat
          reprehenderit rerum ut!</p>
      </div>
      <div class="row">
        <div class="col">
          <table class="table table-hover text-center table-striped">
            <thead class="bg-success text-white">
            <tr>
              <th>Sno</th>
              <th>Name</th>
              <th>Email</th>
              <th>Company</th>
              <th>Website</th>
              <th>Location</th>
            </tr>
            </thead>
            <tbody>
            <tr v-for="fila in usuarios" :key="fila.name">
              <td>{{ fila.id }}</td>
              <td>{{ fila.name }}</td>
              <td>{{ fila.email }}</td>
              <td>{{ fila.company.name }}</td>
              <td>{{ fila.website }}</td>
              <td>{{ fila.address.city }}</td>
            </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { UserService } from "@/services/UserService";

export default {
  name: "UserList",
  data: function() {
    return {
      usuarios: [],
      errorMessage: ''
    };
  },
  created: async function() {
    try {
      let response = await UserService.getAllUsers();
      this.usuarios = response;
    } catch (error) {
      this.errorMessage = error;
    }
  }
};
</script>

<style scoped>

</style>
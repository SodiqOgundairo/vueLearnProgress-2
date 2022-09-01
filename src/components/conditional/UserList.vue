<template>
  <!-- <pre> {{this.IsloggedIn}} </pre> -->
  <div class="container">
    <div class="row">
      <div class="col">
        <p class="h3 text-success fw-bold mt-4">User List</p>
        <p class="fst-itali">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem
          impedit officia enim, unde officiis similique ex ad tempore deserunt
          ab! Necessitatibus, ea doloremque? Omnis, officia repellendus!
          Laborum, quae. Doloribus, ad.
        </p>
      </div>
      <div v-if="loading">
        <Spinner />
      </div>

      <div v-if="errorMessage">
        <p class="h3 text-danger fw-bold fst-italic">{{ errorMessage }}</p>
      </div>

      <div class="row" v-if="!loading && users.length > 0">
        <div class="col">
          <table class="table table-hover text-center table-striped">
            <thead class="bg-success text-white">
              <tr>
                <th>S/No</th>
                <th>Name</th>
                <th>Email</th>
                <th>Company</th>
                <th>Website</th>
                <th>Location</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="user in users" :key="user.id">
                <td>{{ user.id }}</td>
                <td>{{ user.name }}</td>
                <td>{{ user.email }}</td>
                <td>{{ user.company.name }}</td>
                <td>{{ user.website }}</td>
                <td>{{ user.address.city }}</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { UserService } from "./../services/UserService.js";
import Spinner from "./../spinner/Spinner.vue";

export default {
  name: "UserList-vue",

  data() {
    return {
      loading: false,
      // uncomment below to use local data ("./../services/UserService.js")
      // users: UserService.getAllUsers()

      // fetching data via api
      users: [],

      errorMessage: null,
    };
  },

  created: async function () {
    try {
      this.loading = true;
      let response = await UserService.getAllUsers();
      this.loading = false;
      this.users = response.data;
    } catch (error) {
      this.loading = false;
      this.errorMessage = error;
    }
  },

  components: {
    Spinner,
  },
};
</script>

<style></style>

<template>
<!-- <pre> {{this.user}} </pre> -->
  <div class="container mt-3">
    <div class="row">
      <div class="col-md-3">
        <div class="card shadow-lg">
          <div class="card-header bg-success text-white">
            <p class="h3">Register Here</p>
          </div>
          <div class="card-body bg-light">
            <form @submit.prevent="register()" action="">
              <div class="mb-2">
                <input type="text" class="form-control" placeholder="Name" v-model="user.name"/>
              </div>
              <div class="mb-2">
                <input type="text" class="form-control" placeholder="Email" v-model="user.email"/>
              </div>
              <div class="mb-2">
                <input
                  type="password"
                  class="form-control"
                  placeholder="*****" v-model="user.password"
                />
              </div>
              <div class="mb-2">
                <input type="submit" class="btn btn-success shadow-none" value="Register" />
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
  name: "Register-vue",

  data() {
      return {
          user: {
              name: " ",
              email: " ",
              password: " "
          }
      }
  },

  methods: {
      register() {
          console.error(this.user)
      }
  }
};
</script>

<style></style>

<template>
  <!-- <pre> {{this.IsloggedIn}} </pre> -->
  <div class="container">
    <div class="row">
      <div class="col-md-6">
        <div class="card shadow-lg">
          <div class="card-body">
            <div class="mt-2" v-if="IsloggedIn">
              <p class="h3 fw-bold text-success">Welcome User</p>
              <p class="fst-italic">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe
                assumenda, tempora amet illum soluta vitae dolore,
                reprehenderit, nihil veritatis ipsam sunt dolores maxime et
                distinctio quo velit quod impedit nam!
              </p>
            </div>

            <div class="mt-4" v-if="!IsloggedIn">
              <p class="h3 fw-bold text-danger">Thank you!!!</p>
              <p class="fst-italic">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Tempora, suscipit. Sapiente eaque ipsa nobis corrupti ab cumque
                repellendus iste temporibus, similique facere quis fuga velit
                hic molestias necessitatibus, soluta ad.
              </p>
            </div>
            <div class="">
              <button class="btn btn-success btn-sm m-1" @click="IsloggedIn=true" v-if="!IsloggedIn">Login</button>
              <button class="btn btn-danger btn-sm m-1" @click="IsloggedIn=false" v-if="IsloggedIn">Logout</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AuthUser-vue",

  data() {
    return {
      IsloggedIn: false,
    };
  },

};
</script>

<style></style>

<template>
<div class="container mt-3">
    <div class="row">
        <div class="col-md-6">
            <div class="card shadow-lg">
                <div class="card-header">
                    <div class="card-body">
                        <p class="h3">Hello, <span class="fw-bold" >{{this.msg}}</span>  </p>
                        <button class="btn btn-success m-1" @click="greet(value= 'Good Morning') ">Good Morning</button>
                        <button class="btn btn-warning m-1" @click="greet(value= 'Good Afternoon') ">Good Afternoon</button>
                        <button class="btn btn-danger m-1" @click="greet(value= 'Good Evening') ">Good Evening</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
  name: "Greeting-vue",

  data() {
      return {
          msg: ""
      }
  },

  methods : {
      greet(value){
          this.msg = value;
      }
  }

};
</script>

<style></style>

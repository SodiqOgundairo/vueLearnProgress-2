<template>
<div class="container">
    <div class="row">
        <div class="col-md-4">
            <div class="card shadow-lg">
                <div class="card-header">
                    <div class="card-body">
                        <p class="h3 display-3"> {{this.count}} </p>
                        <button class="btn btn-success m-1 shadow-none" @click="count=count+1"> Incremenet </button>
                        <button class="btn btn-warning m-1 shadow-none" @click="count=count-1"> Decremenet </button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
  name: "Counter-vue",

  data() {
      return {
          count: 0
      }
  }
};
</script>

<style></style>

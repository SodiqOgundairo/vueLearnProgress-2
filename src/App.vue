<template>
<Navbar />
  <div class="container mt-3">
    <div class="grid">
      <div class="row">
        <div class="col">
          <p class="h3 text-success fw-bold">App Component</p>
          <p class="fst-italic">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Laboriosam,
            nisi voluptatibus! In ullam rem reiciendis, optio autem animi
            molestiae et exercitationem fugiat ipsam cupiditate! Dignissimos,
            corporis et! Tempora, voluptates iure?
          </p>
        </div>
      </div>
    </div>
    <AuthUser />
    <!-- <UserList /> -->
  </div>
</template>

<script>
import AuthUser from './components/conditional/AuthUser.vue';
// import UserList from './components/conditional/UserList.vue';
import Navbar from './components/navbar/Navbar.vue';

export default {
  name: "App",

  components: {
    AuthUser,
    // UserList,
    Navbar
  },
};
</script>

<style></style>

<template>
<nav class="navbar navbar-dark bg-success navbar-expand-sm"> 
    <div class="container">
        <router-link to="/" class="navbar-brand"> McLamba </router-link>
        <div class="collapse navbar-collapse">
            <ul class="navbar-nav">
                <li class="nav-item">
                    <router-link to="/" class="nav-link px-4">Home</router-link>
                </li>
                <li class="nav-item">
                    <router-link to="/users" class="nav-link px-4">Users</router-link>
                </li>
                <li class="nav-item">
                    <router-link to="/form" class="nav-link px-4">Form</router-link>
                </li>
            </ul>
        </div>
    </div>
</nav>
</template>

<script>
export default {
  name: "Navbar-vue",
};
</script>

<style></style>

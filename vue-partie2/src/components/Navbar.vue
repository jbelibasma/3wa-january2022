<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-dark">
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarText" aria-controls="navbarText" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarText">
    <ul class="navbar-nav mr-auto   m-auto">
      <li class="nav-item active">
        <a class="nav-link text-primary " href="#"> <router-link to="/">home</router-link></a>
      </li>
      <li class="nav-item">
        <a class="nav-link text-primary" href="#"><router-link to="/about">about</router-link></a>
      </li>
      <li class="nav-item">
        <a class="nav-link text-primary" href="#"><router-link to="/contact">contact</router-link></a>
      </li>
    </ul>
  </div>
</nav>
</template>

<script>
export default {
    

}
</script>

<style>

</style>
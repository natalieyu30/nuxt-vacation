<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark padding">
    <div class="container">
      <Nuxt-link class="navbar-brand" to="/">NatDev</Nuxt-link>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse ml-auto"
        id="navbarSupportedContent">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item active">
            <Nuxt-link to="/products" class="nav-link">Place to Stay <span class="sr-only">(current)</span></Nuxt-link>
          </li>
          <li class="nav-item active">
            <Nuxt-link to="/my-items" class="nav-link">My Items <span class="sr-only">(current)</span></Nuxt-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
  export default {
      
  }
</script>

<style scoped>
  .padding {
      padding: 0.5rem;
      background-color: #117710 !important;
  }
  .nav-left {
      margin-left: auto;
  }
</style>
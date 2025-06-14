<script setup>
  import { ref } from 'vue'
  import 'animate.css'

  let num = ref(0)
</script>

<template>
  <div class="body_">
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
      <div class="container-fluid">
        <RouterLink class="navbar-brand" to="/">
          <img src="https://cdn-icons-png.flaticon.com/512/188/188987.png" alt="Logo" width="30" height="24" class="d-inline-block align-text-top">
          PokeVite
        </RouterLink>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <RouterLink class="nav-link" aria-current="page" to="/">Home</RouterLink>
            </li>
            <li class="nav-item">
              <RouterLink class="nav-link" to="/about">About</RouterLink>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <div class="main">
      <RouterView />
    </div>

    <footer class="bg-primary text-light">
      <div>
        Design in {{ new Date().getFullYear() }}
      </div>
    </footer>
  </div>
</template>

<style scoped>
  .body_ {
    height: 100vh;
    background: rgb(106,196,233);
    background: linear-gradient(0deg, rgba(106, 196, 233, 0.9) 0%, rgba(0, 41, 150, 1) 100%);

  }

  footer {
    position: fixed;
    bottom: 0;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 56px;
  }
</style>

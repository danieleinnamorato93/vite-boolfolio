<script>
import { RouterLink } from "vue-router";

export default {
  name: "AppHeader",
  data() {
    return {};
  },
};
</script>

<template>
  <header>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <div class="container-fluid">
        <a class="navbar-brand link-danger" href="#">NavDan</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNavAltMarkup"
          aria-controls="navbarNavAltMarkup"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
          <div class="navbar-nav">
            <li class="me-3">
              <router-link
                class="nav-link active icon-link-hover link-danger"
                :to="{ name: 'home' }"
                >Homepage</router-link
              >
            </li>
            <li class="me-3">
              <router-link class="nav-link link-danger" :to="{ name: 'about' }"
                >About</router-link
              >
            </li>
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>

<style scoped lang="scss">
router-link {
  color: black;
}
</style>

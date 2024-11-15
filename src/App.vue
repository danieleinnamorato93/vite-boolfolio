<script>
import { RouterView } from "vue-router";
import AppFooter from "./components/AppFooter.vue";

import AppHeader from "./components/AppHeader.vue";

//import AppMain from "./pages/AppProjects.vue";
export default {
  data() {
    return {};
  },
  components: {
    AppFooter,
    AppHeader,
  },
};
</script>

<template>
  <AppHeader />
  <RouterView />
  <AppFooter />
</template>

<style lang="scss">
@use "bootstrap/scss/bootstrap.scss" as *;
@use "./style/general.scss" as *;
</style>

<script>
import ProjectsList from "../components/ProjectsList.vue";

export default {
  name: "AppProjects",
  data() {
    return {};
  },
  methods: {},
  created() {
    console.log("app projects caricato");
  },
  components: {
    ProjectsList,
  },
};
</script>

<template>
  <main>
    <div class="container">
      <div class="row">
        <div class="col-12">
          <h1>Projects List:</h1>
        </div>
        <ProjectsList />
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
h1 {
  color: rgb(255, 0, 0);
}
a {
  color: red;
}
</style>

<script>
import axios from "axios";
import ProjectsListCard from "./ProjectsListCard.vue";
import AppLoader from "../components/AppLoader.vue";

export default {
  name: "ProjectsList",
  components: { ProjectsListCard, AppLoader },
  data() {
    return {
      projectsList: [],
      apiUrl: "http://127.0.0.1:8000/api/projects",
      loaded: false,
    };
  },
  methods: {
    getProjects() {
      console.log("avvio chiamata");
      axios
        .get(this.apiUrl)
        .then((response) => {
          console.log("dati ottenuti", response.data.results);
          this.projectsList = response.data.results;
          this.loaded = true;
        })
        .catch(function (error) {
          console.log(error);
        });
    },
  },
  created() {
    this.getProjects();
  },
};
</script>

<template>
  <section class="loader" v-if="!loaded">
    <AppLoader />
  </section>

  <div class="col-12 text-center" v-else>
    <ProjectsListCard
      v-for="singleProject in projectsList"
      :key="singleProject.id"
      :singleProjectObject="singleProject"
    />
  </div>
</template>

<style lang="scss" scoped>
h1 {
  color: white;
}
</style>

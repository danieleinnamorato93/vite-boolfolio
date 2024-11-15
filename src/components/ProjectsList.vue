<script>
import axios from "axios";
import ProjectsListCard from "./ProjectsListCard.vue";
export default {
  name: "ProjectsList",
  components: { ProjectsListCard },
  data() {
    return {
      projectsList: [],
      apiUrl: "http://127.0.0.1:8000/api/projects",
    };
  },
  methods: {
    getProjects() {
      axios
        .get(this.apiUrl)
        .then((response) => {
          console.log(response.data.results);
          this.projectsList = response.data.results;
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
  <div class="col-12 text-center">
    <ProjectsListCard
      v-for="singleProject in projectsList"
      :key="singleProject.id"
      :singleProjectObject="singleProject"
    />
  </div>
</template>

<style scoped>
h1 {
  color: black;
}
a {
  color: red;
}
</style>

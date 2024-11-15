<script>
import axios from "axios";
export default {
  name: "ProjectsList",
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
  <main>
    <div class="container">
      <div class="row">
        <div class="col-12">
          <h1>Projects List:</h1>
        </div>

        <div class="col-12 text-center">
          <div
            class="card bg-primary mb-4 p-3"
            v-for="singleProject in projectsList"
            :key="singleProject.id"
          >
            <div class="card-body">
              <h3 class="card-title">{{ singleProject.title }}</h3>
              <span class="card-title badge text-bg-warning">{{
                singleProject.type.name
              }}</span>
              <a href="{{ singleProject.url }}">
                <h6 class="card-title">{{ singleProject.url }}</h6>
              </a>
              <h4 class="card-title">{{ singleProject.technologies.name }}</h4>
              <p class="card-text">
                {{ singleProject.content }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
h1 {
  color: black;
}
a {
  color: red;
}
</style>

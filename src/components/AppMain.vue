<script>
import axios from "axios";
export default {
  name: "AppMain",
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

        <div class="col-12">
          <div class="card">
            <img src="" class="card-img-top" alt="" />
            <div class="card-body">
              <h5 class="card-title">Card title</h5>
              <p class="card-text">
                Some quick example text to build on the card title and make up
                the bulk of the card's content.
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
</style>

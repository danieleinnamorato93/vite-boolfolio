<script>
export default {
  name: "ProjectsListCard",
  data() {
    return {};
  },
  props: {
    singleProjectObject: {
      type: Object,
      required: true,
    },
  },
};
</script>

<template>
  <article class="card bg-primary mb-4 p-5">
    <div class="card-body">
      <h2 class="card-title">{{ singleProjectObject.title }}</h2>
      <span class="card-title badge text-bg-warning">{{
        singleProjectObject.type.name
      }}</span>
      <a href="{{ singleProjectObject.url }}">
        <h6 class="card-title">{{ singleProjectObject.url }}</h6>
      </a>
      <h4 class="card-title">{{ singleProjectObject.technologies.name }}</h4>
      <p class="card-text">
        {{ singleProjectObject.content }}
      </p>
    </div>
  </article>
</template>

<style scoped lang="scss">
a {
  color: white;
}
</style>

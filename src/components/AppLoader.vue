<script>
export default {
  name: "AppLoader",
  data() {
    return {};
  },
};
</script>

<template>
  <section class="single-loader d-flex py-5">
    <div class="loader m-auto"></div>
  </section>
</template>

<style scoped lang="scss">
/* HTML: <div class="loader"></div> */
.loader {
  display: inline-grid;
  width: 80px;
  aspect-ratio: 1;
  overflow: hidden;
  background: conic-gradient(
      from 146deg at 50% 1%,
      #0000,
      #ec0000 2deg 65deg,
      #0000 68deg
    ) -5% 100%/20% 27% repeat-x;
}
.loader:before {
  content: "";
  margin: 12.5%;
  clip-path: polygon(
    100% 50%,
    78.19% 60.26%,
    88.3% 82.14%,
    65% 75.98%,
    58.68% 99.24%,
    44.79% 79.54%,
    25% 93.3%,
    27.02% 69.28%,
    3.02% 67.1%,
    20% 50%,
    3.02% 32.9%,
    27.02% 30.72%,
    25% 6.7%,
    44.79% 20.46%,
    58.68% 0.76%,
    65% 24.02%,
    88.3% 17.86%,
    78.19% 39.74%
  );
  background: #9e2622;
  animation: l7 3s linear infinite;
  translate: -135% 0;
}
@keyframes l7 {
  to {
    rotate: 400deg;
    translate: 135% 0;
  }
}
</style>

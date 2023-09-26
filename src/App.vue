<script>
import PreviewVue from "./components/Preview.vue";
export default {
  components: {
    PreviewVue,
  },
};
</script>

<template>
  <div class="main__layout">
    <PreviewVue></PreviewVue>
  </div>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Manrope:wght@500;700&family=Overpass:wght@700&display=swap");

.main__layout {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: hsl(210, 46%, 95%);
}
@media (max-width: 719px) {
  .main__layout {
    justify-content: flex-start;
  }
}
</style>

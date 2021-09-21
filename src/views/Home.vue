<template>
  <div class="page-home">
    <h1 class="page-home__title">KenMil Word Counter</h1>
    <word-counter></word-counter>
    <page-footer></page-footer>
  </div>
</template>

<script>
import WordCounter from "../components/WordCounter.vue";
export default {
  name: "Home",
  components: {
    WordCounter
  },
};
</script>

<style scoped>
.page-home {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.page-home__title {
  color: #f5f5f5;
}
</style>
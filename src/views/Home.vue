<template>
  <div class="page-home">
    <h1>KenMil Word Counter</h1>
    <word-counter></word-counter>
    <page-footer></page-footer>
  </div>
</template>

<script>
import WordCounter from "../components/WordCounter.vue";
import PageFooter from "../components/PageFooter.vue";
export default {
  name: "Home",
  components: {
    WordCounter, PageFooter
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
</style>
<template>
  <div>
    <router-view class="router-vue" />
    <page-footer></page-footer>
  </div>
</template>

<script>
import PageFooter from "./components/PageFooter.vue";
export default {
  components: {
    PageFooter
  }
  
}
</script>

<style>
* {
  padding: 0.25rem;
  margin: 0.25rem;
  font-family: Arial, Helvetica, sans-serif;
}

html, body, div {
  padding: 0;
  margin: 0;
}

body {
  background-color: rgb(33, 42, 48);
}
</style>
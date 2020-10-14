<template>
  <div id="test">
    <ol v-for="p in posts" :key="p.id">
      <p>"{{ p.title }}"</p>
    </ol>
  </div>
</template>

<script>
import axios from "axios";

export default {
  props: {
    msg: Array,
  },
  data() {
    return {
      posts: [],
      errors: [],
    };
  },
  created() {
    console.log("cccv");
    this.$store.commit("change", 56),
      axios
        .get(`http://jsonplaceholder.typicode.com/posts`)
        .then((response) => {
          // JSON responses are automatically parsed.

          this.posts = response.data;
        })
        .catch((e) => {
          this.errors.push(e);
        });
  },
};
</script>

<style></style>

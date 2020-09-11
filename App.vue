<template>
  <div id="app">
    <p>Env test parcel</p>
    <h1>{{ name }}</h1>
    <gif />
  </div>
</template>

<script>
import gif from "./components/gif";
export default {
  name: "App",
  data() {
    return {
      name: "testing data in app",
    };
  },
  components: {
    gif,
  },
  mounted() {
    console.log(process.env.VUE_APP_ROOT_ENV);
    console.log("testing some more");
  },
};
</script>

<style lang="scss" scoped></style>

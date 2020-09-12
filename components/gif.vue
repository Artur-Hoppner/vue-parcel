<template>
  <div>
    <h1>show GIF</h1>
    <h1 v-if="development">
      development
    </h1>
    <h1 v-if="production">production</h1>
  </div>
</template>

<script>
export default {
  mounted() {
    console.log(process.env.NODE_ENV);
  },
  computed: {
    development() {
      if (process.env.NODE_ENV == "development") {
        return true;
      }
    },
    production() {
      if (process.env.NODE_ENV == "production") {
        return true;
      }
    },
  },
};
</script>

<style lang="scss"></style>

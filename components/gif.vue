<template>
  <div>
    <h1>show GIF</h1>
    <h1 v-if="(getItRight = true)">
      fuck it works. Good job 100%
    </h1>
  </div>
</template>

<script>
export default {
  mounted() {
    console.log(process.env.NODE_ENV);
  },
  computed: {
    getItRight() {
      if (process.env.NODE_ENV == "production") {
        return true;
      }
    },
  },
};
</script>

<style lang="scss"></style>

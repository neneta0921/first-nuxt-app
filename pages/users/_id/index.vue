<template>
  <h1>A single user, with ID: {{ $route.params.id }}</h1>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  validate(data) {
    return /^\d+$/.test(data.params.id);
  },
  layout: "users",
});
</script>
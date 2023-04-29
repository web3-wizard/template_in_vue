<template>
  <h1>Hello {{ name }} using {{ language }}</h1>
</template>

<script>
export default {
  name: "Greet-name",
  props: ["name", "language"],
};
</script>

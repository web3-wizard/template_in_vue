<template>
  <div>
    <input type="text" v-model="name" />
    <button @click="$emit('close', name)">Close Popup</button>
    <hr />
    <h1>Article Component</h1>
    <h2>{{ title }}</h2>
    <h3>Likes - {{ likes }}</h3>
    <h4>Published - {{ isPublished ? "Yes" : "No" }}</h4>
  </div>
</template>

<script>
export default {
  name: "Article-name",
  props: {
    title: {
      type: String,
      required: true,
      default: "Title Goes here",
    },
    likes: Number,
    isPublished: Boolean,
  },
  emits: {
    close: (name) => {
      if (!name) {
        return false;
      } else {
        return true;
      }
    },
  },
  data() {
    return {
      name: "",
    };
  },
};
</script>

<style lang="scss" scoped></style>

<template>
  <!-- <Greet name="Rahul" language="javascript" /> -->
  <!-- <Greet name="Prabir" language="React native" /> -->
  <!-- <Greet :name="name" :language="language" /> -->
  <Article
    v-show="showPopup"
    title="Article Title"
    :likes="50"
    :isPublished="true"
    @close="closePopup"
  />

  <hr />
  <button @click="showPopup = true">Show Popup</button>
  <hr />
  <!-- <input type="text" v-model="name" /> -->
  <Input v-model="name" />

  <hr />
  <Card> Card Content </Card>
  <Card> <h2>Card Content</h2> </Card>
  <Card>
    <template v-slot:header>
      <h3>Header</h3>
    </template>
    <template v-slot:default>
      <img src="http://picsum.photos/200" />
    </template>
    <template v-slot:footer>
      <button>View Details</button>
    </template>
  </Card>
</template>

<script>
// import Greet from "./components/Greet.vue";
import Article from "./components/Article.vue";
import Input from "./components/Input.vue";
import Card from "./components/Card.vue";

export default {
  name: "App",
  components: {
    // Greet,
    Article,
    Input,
    Card,
  },
  data() {
    return {
      // name: "Web3_wizard",
      // language: "Solidity",
      showPopup: false,
      name: "",
    };
  },
  methods: {
    closePopup(name) {
      this.showPopup = false;
      console.log("name : " + name);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

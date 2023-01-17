<template>
  <div id="container">
    <TabMenu />
    <Footer />
  </div>
</template>

<script>
import TabMenu from "./components/TabMenu.vue";
import Footer from "./components/FootBar.vue";

export default {
  name: "App",
  components: {
    TabMenu,
    Footer,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#container {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

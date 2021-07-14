<template>
  <div id="app">
    <Header class="header" />
    <Main class="my-container" :songs="songs" />
  </div>
</template>

<script>
import axios from "axios";
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
  },
  data() {
    return {
      songs: [],
    };
  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((res) => {
        this.songs = res.data.response;
      });
  },
};
</script>

<style lang="scss">
#app {
  background-color: #1e2d3b;
  height: 100vh;
  .header {
    height: 48px;
    padding: 12px 24px;
    background-color: #2e3a46;
  }
  .my-container {
    width: 300px;
    height: calc(100% - 48px);
    margin: 0 auto;
    padding: 24px 0;
    overflow-y: auto;
  }
  @media screen and (min-width: 600px) {
    .my-container {
      width: 500px;
    }
  }
  @media screen and (min-width: 900px) {
    .my-container {
      width: 800px;
    }
  }
}
</style>

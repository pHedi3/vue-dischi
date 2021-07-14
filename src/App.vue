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
  min-height: 100vh;
  .header {
    height: 48px;
    padding: 12px 24px;
    background-color: #2e3a46;
  }
  .my-container {
    width: 800px;
    height: calc(100% - 40px);
    margin: 0 auto;
    padding: 24px 0;
  }
}
</style>

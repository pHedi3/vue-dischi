<template>
  <div class="song-box">
    <div class="song">
      <img :src="poster" alt="" />
      <div class="title">
        {{ title }}
      </div>
      <div class="more-info">
        {{ author }}<br />
        {{ year }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Song",
  props: {
    poster: String,
    title: String,
    author: String,
    year: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.song-box {
  width: calc(100% / 2 - 24px);
  padding: 12px;
  margin: 12px;
  background-color: #2e3a46;
  height: 280px;
  text-align: center;
  .song {
    width: 100%;
    img {
      width: 100%;
      margin-bottom: 12px;
    }
    .title {
      color: white;
      font-weight: bold;
      font-size: 16px;
      margin-bottom: 12px;
    }
    .more-info {
      color: #687778;
      font-size: 12px;
    }
  }
}
@media screen and (min-width: 600px) {
  .song-box {
    width: calc(100% / 3 - 24px);
  }
}
@media screen and (min-width: 900px) {
  .song-box {
    width: calc(100% / 5 - 24px);
  }
}
</style>
<template>
  <div class="my-row">
    <Song
      v-for="(song, index) in songs"
      :key="index"
      :poster="song.poster"
      :title="song.title"
      :author="song.author"
      :year="song.year"
    />
  </div>
</template>

<script>
import Song from "./Song.vue";
export default {
  name: "Main",
  components: {
    Song,
  },
  props: {
    songs: Array,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.my-row {
  display: flex;
  flex-wrap: wrap;
}
</style>
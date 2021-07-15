<template>
  <div>
    <img src="../assets/spotify-logo.png" alt="" />
    <div>
      <select v-model="gen" @change="$emit('gen', gen)">
        <option value="All">ALL</option>
        <option value="Rock">Rock</option>
        <option value="Metal">Metal</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
      </select>
      <input
        type="text"
        placeholder="cerca la canzone"
        v-model="songSerch"
        @keyup.enter="$emit('songSerch', songSerch)"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      gen: "",
      songSerch: "",
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
div {
  display: flex;
  justify-content: space-between;
  img {
    height: 100%;
  }
  select {
    width: 80px;
    margin-right: 12px;
  }
}
</style>
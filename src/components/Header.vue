<template>
  <div>
    <img src="../assets/spotify-logo.png" alt="" />
    <select v-model="gen" @change="$emit('gen', gen)">
      <option value="All">ALL</option>
      <option value="Rock">Rock</option>
      <option value="Metal">Metal</option>
      <option value="Pop">Pop</option>
      <option value="Jazz">Jazz</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      gen: "",
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
img {
  height: 100%;
}
</style>
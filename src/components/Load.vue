<template>
  <div class="load">Sto Caricando</div>
</template>

<script>
export default {
  name: "Load",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.load {
  position: fixed;
  top: 20px;
  left: 50%;
  transform: translate(-50%);
  color: white;
  font-size: 30px;
}
</style>
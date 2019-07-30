<template>
  <div class="display-area">
    <div class="text">{{ line }}</div>
  </div>
</template>

<script>
// eslint-disable-next-line no-console
export default {
  name: "Inputbutton",
  props: {
    line: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.display-area {
  background-color: #2e3440;
  display: flex;
  align-items: center;
}
.text {
  width: 100%;
  padding: 0 20px;
  color: #eceff4;
  font-size: 35px;
  font-weight: 800;
  text-align: right;
}
</style>

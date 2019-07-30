<template>
  <div class="display-area"></div>
</template>

<script>
// eslint-disable-next-line no-console
export default {
  name: "Inputbutton",
  props: {
    role: String
  },
  methods: {
    clickAction() {
      // eslint-disable-next-line no-console
      console.log(`clicked ${this.role}`);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.display-area {
  background-color: #2e3440;
}
</style>

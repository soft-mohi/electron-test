<template>
  <button class="input-button" @click="clickAction">{{ role }}</button>
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
      this.$emit("keyPress", `${this.role}`);
      // eslint-disable-next-line no-console
      console.log(`clicked ${this.role}`);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
.input-button {
  background-color: transparent;
  border: none;
  cursor: pointer;
  outline: none;
  padding: 0;
  appearance: none;
  display: inline-block;
  width: 100%;
  height: 100%;
  background-color: #4c566a;
  color: #eceff4;
  font-size: 20px;
  font-weight: 600;
}
</style>

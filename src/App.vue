<template>
  <div id="app">
    <div class="container">
      <display-area id="display-area" :line="buf"></display-area>
      <input-button @keyPress="onPress" id="button-C" :role="'C'"></input-button>
      <input-button @keyPress="onPress" id="button-plusminus" :role="'±'"></input-button>
      <input-button @keyPress="onPress" id="button-per" :role="'%'"></input-button>
      <input-button @keyPress="onPress" id="button-9" :role="'9'"></input-button>
      <input-button @keyPress="onPress" id="button-8" :role="'8'"></input-button>
      <input-button @keyPress="onPress" id="button-7" :role="'7'"></input-button>
      <input-button @keyPress="onPress" id="button-6" :role="'6'"></input-button>
      <input-button @keyPress="onPress" id="button-5" :role="'5'"></input-button>
      <input-button @keyPress="onPress" id="button-4" :role="'4'"></input-button>
      <input-button @keyPress="onPress" id="button-3" :role="'3'"></input-button>
      <input-button @keyPress="onPress" id="button-2" :role="'2'"></input-button>
      <input-button @keyPress="onPress" id="button-1" :role="'1'"></input-button>
      <input-button @keyPress="onPress" id="button-0" :role="'0'"></input-button>
      <input-button @keyPress="onPress" id="button-dot" :role="'.'"></input-button>
      <input-button @keyPress="onPress" id="button-div" :role="'÷'"></input-button>
      <input-button @keyPress="onPress" id="button-mul" :role="'×'"></input-button>
      <input-button @keyPress="onPress" id="button-plus" :role="'ー'"></input-button>
      <input-button @keyPress="onPress" id="button-minus" :role="'＋'"></input-button>
      <input-button @keyPress="onPress" id="button-eq" :role="'＝'"></input-button>
    </div>
  </div>
</template>

<script>
import InputButton from "./components/InputButton.vue";
import DisplayArea from "./components/DisplayArea.vue";

export default {
  name: "app",
  components: {
    InputButton,
    DisplayArea
  },
  data: function() {
    return {
      buf: ""
    };
  },
  methods: {
    onPress(key) {
      this.buf = `clicked:${key}`;
    }
  }
};
</script>

<style>
#app {
  overflow: hidden;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
}

.container {
  position: relative;
  width: 100%;
  height: 100%;
  display: grid;
  grid-template-rows: 100px 1fr 1fr 1fr 1fr 1fr;
  grid-template-columns: 1fr 1fr 1fr 1fr;
}

#display-area {
  grid-column: 1 / 5;
}

#button-C {
}
#button-plusminus {
}
#button-per {
}
#button-9 {
}
#button-8 {
}
#button-7 {
}
#button-6 {
}
#button-5 {
}
#button-4 {
}
#button-3 {
}
#button-2 {
}
#button-1 {
}
#button-0 {
  grid-column: 1/3;
}
#button-dot {
}
#button-div {
  grid-column: 4/5;
  grid-row: 2/3;
}
#button-mul {
  grid-column: 4/5;
  grid-row: 3/4;
}
#button-plus {
  grid-column: 4/5;
  grid-row: 4/5;
}
#button-minus {
  grid-column: 4/5;
  grid-row: 5/6;
}
#button-eq {
  grid-column: 4/5;
  grid-row: 6/7;
}
</style>

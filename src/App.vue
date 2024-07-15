<template>
  <div id="app">
    <div class="window">
      <ProgressBar
        :max="108"
        :threshold="80"
        :value="value"
        text="Ещё продать на завтра"
        unit="ч"
      />
    </div>
    <input type="number" v-model.number="newValue" />
    <button @click="value = newValue">Установить значение:</button>
  </div>
</template>

<script>
import ProgressBar from "./components/ProgressBar.vue";

export default {
  name: "App",
  data() {
    return {
      value: 35,
      newValue: 35
    };
  },
  components: {
    ProgressBar,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

body {
  background-color: #3e4b5c;
}

.window {
  width: 500px;
  height: 500px;
}
</style>

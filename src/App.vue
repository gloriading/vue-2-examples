<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <main>
      <Example />
      <ExampleComposition />
    </main>
  </div>
</template>

<script>
import Example from "./components/Example.vue";
import ExampleComposition from "./components/ExampleComposition.vue";

export default {
  name: "App",
  components: {
    Example,
    ExampleComposition,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  min-height: 100vh;
  padding: 1rem;
}
#app > img {
  height: 80px;
}
main {
  display: flex;
  gap: 1rem;
}
main > * {
  flex: 1;
  border: 1px solid;
}
input[type="text"] {
  border: none;
  outline: none;
  font-size: 1rem;
  line-height: 1.5;
  padding: 8px 16px;
}
button {
  padding: 8px 16px;
  border: 1px solid lightgrey;
  outline: none;
  background-color: #fff;
  cursor: pointer;
}
</style>

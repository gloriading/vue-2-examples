<template>
  <div>
    <h1>Vue 2 options api examples</h1>
    <section>
      <h3>Basics</h3>
      <p>
        My name is {{ name }}
        <button @click="sayHi">Say Hi</button>
      </p>
      <p v-show="hiMessage">{{ hiMessage }}</p>
    </section>

    <section>
      <div class="inputs">
        <InputFieldA /><!-- no interaction with child -->
        <InputFieldB /><!-- no interaction with child -->
        <InputFieldC @childToParent="handleChildMessage" />
        <InputFieldD v-model="title" />
        <InputFieldE v-model="description" />
        <InputFieldF v-model="content" />
        <InputFieldG v-model="names" />
      </div>

      <div class="display">
        <button @click="clearInputs">Clear</button>

        <p v-show="childMessage">Child message: {{ childMessage }}</p>
      </div>
    </section>
  </div>
</template>

<script>
import InputFieldA from "./inputs/InputFieldA";
import InputFieldB from "./inputs/InputFieldB";
import InputFieldC from "./inputs/InputFieldC";
import InputFieldD from "./inputs/InputFieldD";
import InputFieldE from "./inputs/InputFieldE";
import InputFieldF from "./inputs/InputFieldF";
import InputFieldG from "./inputs/InputFieldG";

export default {
  components: {
    InputFieldA,
    InputFieldB,
    InputFieldC,
    InputFieldD,
    InputFieldE,
    InputFieldF,
    InputFieldG,
  },
  data() {
    return {
      name: "John Doe",
      age: 12,
      hiMessage: "",
      childMessage: "",
      title: "",
      description: "",
      content: "",
      names: {
        firstName: "",
        lastName: "",
      },
    };
  },
  methods: {
    sayHi() {
      this.hiMessage = "Helloooo";
    },
    handleChildMessage(message) {
      this.childMessage = message;
    },
    clearInputs() {
      this.names = {
        firstName: "",
        lastName: "",
      };
    },
  },
};
</script>

<style scoped>
section {
  text-align: left;
  margin: 1rem;
  padding: 1rem;
  border: 1px solid pink;
}
.inputs {
  margin-top: 1rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 4px;
}
.display {
  margin-top: 1rem;
}
</style>

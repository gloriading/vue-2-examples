<template>
  <div>
    <h1>Vue 2 composition api examples</h1>
    <p>Hi, my name is {{ name }} <button @click="sayHi">Say Hi</button></p>

    <p v-show="message">{{ message }}</p>
  </div>
</template>

<script>
import { ref } from "@vue/composition-api";

export default {
  setup() {
    const name = ref("Cindy");
    const message = ref("");
    const sayHi = () => {
      message.value = "What's up yo!";
    };

    return {
      name,
      message,
      sayHi,
    };
  },
};
</script>

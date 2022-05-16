<template>
  <div>
    <wrapper>
      <template slot="top">
        <InputFieldG v-model="names" />
        <!-- <InputFieldG v-model="addresses" /> -->
      </template>

      <template slot="bottom">
        <button>Submit</button>
      </template>
    </wrapper>

    <p>I got: {{ names.firstName }} {{ names.lastName }}</p>
  </div>
</template>

<script>
import Wrapper from "./Wrapper.vue";
import InputFieldG from "./inputs/InputFieldG.vue";

export default {
  data() {
    return {
      names: {
        firstName: "",
        lastName: "",
      },
    };
  },
  components: {
    Wrapper,
    InputFieldG,
  },
};
</script>

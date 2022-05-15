<template>
  <input
    type="text"
    class="custom"
    :value="myInput"
    @input="handleInput"
    placeholder="custom input B"
  />
</template>
<script>
export default {
  data() {
    return {
      myInput: "",
    };
  },
  methods: {
    handleInput(e) {
      this.myInput = e.target.value;
    },
  },
};
</script>
<style scoped>
.custom {
  border: 1px solid lightgrey;
}
</style>

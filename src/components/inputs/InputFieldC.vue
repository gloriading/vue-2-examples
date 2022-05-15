<template>
  <input
    type="text"
    class="custom"
    v-model="myInput"
    @keyup="emitToParent"
    placeholder="custom input C"
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
    emitToParent() {
      this.$emit("childToParent", this.myInput);
    },
  },
};
</script>
<style scoped>
.custom {
  border: 1px solid lightgrey;
}
</style>

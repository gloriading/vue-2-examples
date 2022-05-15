<template>
  <div>
    <input
      type="text"
      class="custom"
      v-model="myInput"
      placeholder="custom input F"
    />
    <p>{{ myInput }}</p>
  </div>
</template>
<script>
export default {
  props: ["value"],

  computed: {
    myInput: {
      get() {
        return this.value;
      },
      set(val) {
        this.$emit("input", val);
      },
    },
  },
};
</script>
<style scoped>
.custom {
  border: 1px solid lightgrey;
}
</style>

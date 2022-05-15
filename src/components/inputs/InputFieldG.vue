<template>
  <div>
    <input
      type="text"
      class="custom"
      :value="value.firstName"
      name="firstName"
      @input="handleUpdate"
      placeholder="custom input G - 1"
    />
    <input
      type="text"
      class="custom"
      :value="value.lastName"
      name="lastName"
      @input="handleUpdate"
      placeholder="custom input G - 2"
    />
    <p>{{ value.firstName }} {{ value.lastName }}</p>
  </div>
</template>

<script>
export default {
  props: ["value"],
  methods: {
    handleUpdate(e) {
      this.$emit("input", {
        ...this.value,
        [e.target.name]: e.target.value,
      });
    },
  },
};
</script>

<style scoped>
.custom {
  border: 1px solid lightgrey;
}
</style>

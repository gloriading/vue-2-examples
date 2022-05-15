<template>
  <div>
    <input
      type="text"
      class="custom"
      :value="customValue"
      @input="$emit('customInput', $event.target.value)"
      placeholder="custom input E"
    />
    <p>{{ customValue }}</p>
  </div>
</template>
<script>
export default {
  props: ["customValue"],
  // https://v2.vuejs.org/v2/api/#model
  model: {
    prop: "customValue", // default is value
    event: "customInput", // default is input
  },
};
</script>
<style scoped>
.custom {
  border: 1px solid lightgrey;
}
</style>

<template>
  <div>
    <input
      type="text"
      class="custom"
      :value="value"
      @input="$emit('input', $event.target.value)"
      placeholder="custom input D"
    />
    <p>{{ value }}</p>
  </div>
</template>
<script>
export default {
  props: ["value"],
};
</script>
<style scoped>
.custom {
  border: 1px solid lightgrey;
}
</style>

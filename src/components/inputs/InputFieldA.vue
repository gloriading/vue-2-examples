<template>
  <input
    type="text"
    class="custom"
    v-model="myInput"
    placeholder="custom input A"
  />
</template>
<script>
export default {
  data() {
    return {
      myInput: "",
    };
  },
};
</script>
<style scoped>
.custom {
  border: 1px solid lightgrey;
}
</style>

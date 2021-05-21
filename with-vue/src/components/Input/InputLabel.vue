<template>
  <label>{{ text }}</label>
</template>

<script>
module.exports = {
  name: "InputLabels",
  props: ["text"], //← Value passed from parent element.
};
</script>

<style scoped>
label {
  text-transform: uppercase;
  margin: 2rem 0 1rem;
  font-weight: bold;
}
@media only screen and (min-width: 800px) {
  label {
    margin: 3rem 0 1rem;
    font-size: 1.3rem;
  }
}
</style>
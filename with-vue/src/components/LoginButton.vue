<template>
  <button type="submit">{{ isLogin }}</button>
</template>

<script>
module.exports = {
  name: "Button",

  data() {
    return {
      isLogin: "LOG IN",
    };
  },
};
</script>

<style scoped>
button {
  display: block;
  width: 100%;
  max-width: 180px;
  margin: 0 auto;
  padding: 0.5rem;
  background-color: navy;
  color: white;
  border-radius: 5px;
  font-weight: bolder;
}
@media only screen and (min-width: 474px) {
  button {
    max-width: 210px;
  }
}
@media only screen and (min-width: 600px) {
  button {
    padding: 0.7rem;
    max-width: 250px;
  }
}
@media only screen and (min-width: 700px) {
  button {
    padding: 0.8rem;
    max-width: 300px;
  }
}
@media only screen and (min-width: 800px) {
  button {
    font-size: 1rem;
    padding: 0.8rem;
    max-width: 350px;
  }
}
@media only screen and (min-width: 900px) {
  button {
    max-width: 400px;
  }
}
</style>


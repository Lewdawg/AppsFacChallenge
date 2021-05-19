<template>
  <h1>{{ pageTitle }}</h1>
</template>

<script>
module.exports = {
  name: "Title",
  data: function () {
    return {
      pageTitle: "MY MILL",
    };
  },
};
</script>


<style scoped>
h1 {
  text-align: center;
  font-size: 2.5rem;
  padding: 5.5rem 0 1.5rem;
  font-weight: bold;
}
@media only screen and (min-width: 400px) {
  h1 {
    padding: 5rem 6rem 1.5rem 0;
  }
}
@media only screen and (min-width: 474px) {
  h1 {
    padding: 5rem 7rem 1.5rem 0;
  }
}
@media only screen and (min-width: 600px) {
  h1 {
    padding: 5.5rem 11rem 1.5rem 0;
  }
}
@media only screen and (min-width: 700px) {
  h1 {
    padding: 5.5rem 16rem 1.5rem 0;
    font-size: 3rem;
  }
}
@media only screen and (min-width: 800px) {
  h1 {
    padding: 6rem 19rem 1.5rem 0;
    font-size: 3.3rem;
  }
}
@media only screen and (min-width: 900px) {
  h1 {
    padding: 6rem 21rem 1.5rem 0;
  }
}
</style>


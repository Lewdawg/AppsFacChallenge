<template>
  <div id="recoverPass">
    <p>{{ message }} <img src="../assets/lock.svg" alt="" /></p>
  </div>
</template>

<script>
module.exports = {
  name: "RecoverPass",
  data: function () {
    return {
      message: "Forgot password? Recover here",
    };
  },
};
</script>

<style scoped>
#recoverPass {
  display: flex;
  justify-content: center;
  font-size: 10px;
  margin: 1rem 0;
}
@media only screen and (min-width: 474px) {
  #recoverPass {
    font-size: 11px;
  }
}
@media only screen and (min-width: 700px) {
  #recoverPass {
    font-size: 12px;
    margin: 1rem 0 2.5rem;
  }
}
@media only screen and (min-width: 800px) {
  #recoverPass {
    font-size: 14px;
    margin: 1rem 0 3rem;
  }
}
@media only screen and (min-width: 900px) {
  #recoverPass {
    font-size: 16px;
    margin: 1.5rem 0 4rem;
  }
}
</style>
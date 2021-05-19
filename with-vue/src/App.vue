<template>
  <form action="#">
    <Title />
    <Input-fields />
    <Recover-pass />
    <Checkbox />
    <Login-button @isActive="updateButton" />
  </form>
</template>

<script>
import Title from "./components/Title";
import InputFields from "./components/Input/InputFields";
import RecoverPass from "./components/RecoverPass";
import Checkbox from "./components/Checkbox";
import LoginButton from "./components/LoginButton";

export default {
  name: "App",
  data() {
    return {};
  },
  components: {
    Title,
    InputFields,
    RecoverPass,
    Checkbox,
    LoginButton,
  },
};
</script>

<style>
form {
  height: 90vh;
  width: 87vw;
  margin: 5vh auto;
  background-color: white;
  overflow: auto;
}
@media only screen and (min-width: 1040px) {
  form {
    max-width: 58rem;
  }
}
</style>

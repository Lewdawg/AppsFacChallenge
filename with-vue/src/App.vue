<template>
  <form action="#">
    <Title />
    <Input-fields />
    <Recover-pass />
    <Checkbox @input="updateButton" />
    <Login-button v-model="showButton" v-if="showButton" />
  </form>
</template>

// @input - listening out for an 'input' event and when it hears that event triggers it's own method.
// v-model in a nutshell - holds current value and accept's new value when changed.

<script>
import Title from "./components/Title";
import InputFields from "./components/Input/InputFields";
import RecoverPass from "./components/RecoverPass";
import Checkbox from "./components/Checkbox";
import LoginButton from "./components/LoginButton";

export default {
  name: "App",
  data() {
    return {
      showButton: true,
    };
  },
  methods: {
    updateButton() {
      this.showButton = !this.showButton;
      console.log("I come from App.vue", this.showButton);
    },
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

<template>
  <div id="inputFields">
    <Input-label text="e-mail" />
    <input type="email" placeholder="Enter email" />

    <Input-label text="password" />
    <div id="eyePosition">
      <input
        :type="passwordFieldType"
        v-model="password"
        placeholder="Enter password"
      />
      <img @click="showPassword" src="../../assets/eye.svg" alt="" />
    </div>
  </div>
</template>


<script>
import InputLabel from "./InputLabel";

//(line 9)':' keeps the type attribute (or any other) up to date with the value of the passwordFieldType property. (in this case)

export default {
  name: "InputFields",
  data() {
    return {
      password: "", //←Keeps value up to date, if you add text will show it by default
      passwordFieldType: "password", // ←Default setting password
    };
  },
  methods: {
    showPassword() {
      //↓ onclick setting passwordFieldType to opposite of what is current
      this.passwordFieldType =
        this.passwordFieldType === "password" ? "text" : "password";
    },
  },
  components: {
    InputLabel,
  },
};
</script>

<style scoped>
#inputFields {
  display: flex;
  flex-direction: column;
  max-width: 200px;
  margin: 0 auto;
}
#inputFields input {
  padding-left: 1rem;
  font-size: 1.2rem;
  height: 4vh;
  background-color: rgb(240, 240, 240);
  border: none;
  border-bottom: 2px solid navy;
  width: 100%;
}
#eyePosition {
  position: relative;
}
#eyePosition img {
  position: absolute;
  bottom: 5px;
  right: 10px;
  height: 25px;
}
@media only screen and (min-width: 474px) {
  #inputFields {
    max-width: 225px;
  }
}
@media only screen and (min-width: 600px) {
  #inputFields {
    max-width: 275px;
  }
}
@media only screen and (min-width: 700px) {
  #inputFields {
    max-width: 375px;
  }
  #inputFields input {
    height: 5vh;
  }
  #eyePosition img {
    height: 35px;
  }
}
@media only screen and (min-width: 800px) {
  #inputFields label {
    margin: 3rem 0 1rem;
    font-size: 1.3rem;
  }
  #inputFields {
    max-width: 425px;
  }
}
@media only screen and (min-width: 900px) {
  #inputFields {
    max-width: 475px;
  }
  #eyePosition img {
    bottom: 5px;
    right: 10px;
    height: 35px;
  }
}
@media only screen and (min-width: 1040px) {
  #eyePosition img {
    bottom: 6px;
    right: 15px;
  }
}
</style>
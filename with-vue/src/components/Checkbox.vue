<template>
  <div id="checkbox">
    <input
      id="tAndc"
      v-model="isActive"
      type="checkbox"
      name="tAndc"
      @click="noTandC"
      :class="{ active: isActive }"
    />
    <label for="tAndc">{{ terms }}</label>
  </div>
</template>

<script>
module.exports = {
  name: "Checkbox",
  data: function () {
    return {
      isActive: true,
      terms: "I agree to the TERMS AND CONDITIONS",
    };
  },
  Methods: {
    return: {
      noTandC() {
        if (this.isActive === false) {
          this.$emit(isActive);
        }
      },
    },
  },
};
</script>

<style scoped>
label {
  position: relative;
  padding-left: 15px;
}
label:before {
  content: "";
  outline: 1px solid black;
  display: block;
  width: 4px;
  height: 4px;
  position: absolute;
  left: 5px;
  bottom: 3px;
}

#tAndc:checked + label:before {
  background-color: navy;
}

#tAndc {
  display: none; /* ← Hides the defaul checkbox */
}

#checkbox {
  display: flex;
  justify-content: center;
  font-size: 8px;
  margin: 2rem 0 1rem;
}

@media only screen and (min-width: 474px) {
  #checkbox {
    font-size: 9px;
    margin: 2rem 0 1.2rem;
  }
  label:before {
    width: 6px;
    height: 6px;
    left: 4px;
  }
}
@media only screen and (min-width: 600px) {
  #checkbox {
    margin: 2.2rem 0 1rem;
  }
  label:before {
    width: 8px;
    height: 8px;
    left: 0;
    bottom: 2px;
  }
}
@media only screen and (min-width: 700px) {
  #checkbox {
    font-size: 13px;
  }
  label:before {
    width: 8px;
    height: 8px;
    bottom: 4px;
  }
}
@media only screen and (min-width: 800px) {
  #checkbox {
    font-size: 15px;
  }
  label:before {
    width: 10px;
    height: 10px;
    left: -3px;
    bottom: 4px;
  }
}
@media only screen and (min-width: 900px) {
  #checkbox {
    font-size: 16px;
  }
  label:before {
    left: -5px;
    bottom: 5px;
  }
}
</style>
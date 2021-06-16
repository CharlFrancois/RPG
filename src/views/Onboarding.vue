<template>
  <div class="onboarding">
    <img
      src="@/assets/arrow-left.svg"
      v-if="showBeforeButton"
      class="button button-before"
      @click="currentStep--"
    />
    <select-character v-if="currentStep === 0" @selected="storeCharacter" />
    <select-gender v-if="currentStep === 1" />
    <select-armor v-if="currentStep === 2" />
    <select-skills v-if="currentStep === 3" />
    <img
      src="@/assets/arrow-right.svg"
      v-if="showNextButton"
      class="button button-next"
      @click="currentStep++"
    />
  </div>
</template>

<script>
import SelectArmor from "../components/onboarding/SelectArmor.vue";
import SelectCharacter from "../components/onboarding/SelectCharacter.vue";
import SelectGender from "../components/onboarding/SelectGender.vue";
import SelectSkills from "../components/onboarding/SelectSkills.vue";

export default {
  name: "Onboarding",
  components: {
    SelectCharacter,
    SelectGender,
    SelectArmor,
    SelectSkills,
  },
  data() {
    return {
      currentStep: 0,
    };
  },
  computed: {
    showBeforeButton() {
      return this.currentStep !== 0;
    },
    showNextButton() {
      return this.currentStep !== 3;
    },
  },
  created () {
    var audio = new Audio(require('../assets/musique-du-gouffre-de-helm.mp3'));
    audio.play()
  },
  methods: {
    storeCharacter(character) {
      console.log(character);
    },
  },
};
</script>

<style lang="scss" scoped>
.onboarding {
  width: 100vw;
  height: 100vh;
  background-image: url("../assets/background.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
  justify-content: space-around;
  place-items: center;
  .button {
    color: white;
    height: 10rem;
    cursor: pointer;
    &-next {
      position: fixed;
      bottom: 50%;
      right: 0;
    }

    &-before {
      position: fixed;
      bottom: 50%;
      left: 0;
    }
  }
}
</style>
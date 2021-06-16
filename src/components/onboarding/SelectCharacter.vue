<template>
  <div class="select-character">
    <img class="skill" @click="selectedCharacter('skill1')" src="@/assets/skill1.png" />
    <img class="skill" @click="selectedCharacter('skill2')" src="@/assets/skill2.png" />
    <img class="skill" @click="selectedCharacter('skill3')" src="@/assets/skill3.png" />
  </div>
</template>

<script>
export default {
  name: "SelectCharacter",
  methods: {
    selectedCharacter(character) {
      this.$emit("selected", character);
    },
  },
};
</script>

<style lang="scss" scoped>
.select-character {
  background: rgba(black, 0.7);
  border-radius: 10px;
  display: flex;
  justify-content: space-around;
  .skill {
    margin: 1rem;
    cursor: pointer;
    // border: 3px solid orange;
  }
}
</style>

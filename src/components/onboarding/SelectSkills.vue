<template>
  <div class="select-skills">
    <img class="skill-img" src="@/assets/skill1.png" />
    <div class="skills">
      <div class="skill">
        <span class="text">Dextérité</span>
        <div class="progress-bar">
          <div class="progress-pourcentage"></div>
        </div>
      </div>
      <div class="skill">
        <span class="text">Force</span>
        <div class="progress-bar">
          <div class="progress-pourcentage"></div>
        </div>
      </div>
      <div class="skill">
        <span class="text">Vitalité</span>
        <div class="progress-bar">
          <div class="progress-pourcentage"></div>
        </div>
      </div>
      <div class="skill">
        <span class="text">Magie</span>
        <div class="progress-bar">
          <div class="progress-pourcentage"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SelectSkills",
};
</script>

<style lang="scss" scoped>
.select-skills {
  display: flex;
  background: rgba(black, 0.7);
  border-radius: 10px;
  .skills {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    padding: 1rem;
    .skill {
      display: flex;
      flex-direction: column;
      .text {
        color: white;
      }
      .progress-bar {
        width: 10rem;
        height: 1rem;
        background-color: white;
      }
    }
  }
}
</style>

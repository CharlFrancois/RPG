<template>
  <div id="app">
    <onboarding />
  </div>
</template>

<script>
import Onboarding from "./views/Onboarding.vue";

export default {
  name: "App",
  components: {
    Onboarding,
  }
};
</script>

<style>
#app {
  margin: 0px;
}
</style>
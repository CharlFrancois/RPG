<template>
  <div id="app">
    <audio src="/../assests/musique-du-gouffre-de-helm.mp3" autoplay>
      <p>If you are reading this, it is because your browser does not support the audio element.     </p>
    </audio>
   
    <onboarding />
  </div>
</template>

<script>
import Onboarding from './views/Onboarding.vue'

export default {
  name: 'App',
  components: {
    Onboarding
  }
}
</script>

<style>
#app {
  margin: 0px;
}
</style>
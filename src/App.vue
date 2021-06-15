<template>
  <div id="app">
      <div class="container">

          <flower-text />
          <card-figma />
        
      </div>
      
  </div>
</template>

<script>
import CardFigma from './components/CardFigma.vue';
import FlowerText from './components/FlowerText.vue';

export default {
  name: "App",
  components: {
    FlowerText,
    CardFigma
  },
};
</script>

<style>
#app{
   
}
.container {
  position: relative;
  display: flex;
  align-items: center;
  margin: 0;
}
</style>

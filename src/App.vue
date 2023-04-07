<template>
  <body>
    <MyPlant :plantes="plantes" title="🌿  PLANTS  🌿"/>
  </body>
</template>

<script setup>
import MyPlant from './MyPlant.vue';

</script>

<style scoped>

body {
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  height: 50%;
  width: 100%;
  margin: 0 auto;
  background-color: rgb(244, 201, 186);
 
}
</style>
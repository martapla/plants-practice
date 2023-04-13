<template>
  <body>
    
    <MyPlant  :nameprops="plantList[0]" title="🌿  PLANTS  🌿"/>
    <MyPlant  :nameprops="plantList[1]" />
    <MyPlant  :nameprops="plantList[2]" />

    <!-- Plant List shown with v-for: -->
    <!-- <MyPlant  v-for="(plantArr,index) in plantList" :key="index" :nameprops="plantArr"/> -->    

  </body>
</template>

<script setup>
import { ref } from 'vue';
import MyPlant from './components/MyPlant.vue';

const plantList = ref([
  {
    name: 'Fern',
    description: ' The fern is a type of plant that has fronds instead of leaves, and reproduces through spores instead of seeds. It is a common sight in gardens and forests, and its delicate appearance belies its hardiness and ability to thrive in diverse environments.',
    image: 'https://images.unsplash.com/photo-1599416024757-71334210456b?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Nnx8ZmVybnxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60'
  },
  {
    name: 'Cactus',
    description: 'A cactus is a type of succulent plant that is adapted to hot and dry environments. Its characteristic thick and fleshy stem is covered in spines, which help to deter predators and reduce water loss. Despite its prickly exterior, many species of cactus produce beautiful flowers and fruits, and some even have medicinal properties.',
    image: 'https://images.unsplash.com/photo-1554631221-f9603e6808be?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NXx8Y2FjdHVzfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
  },
  {
    name: 'Monstera',
    description: 'The monstera deliciosa, also known as the Swiss cheese plant, is a tropical plant with large, glossy leaves. It requires bright, indirect light and regular watering.',
    image: 'https://images.unsplash.com/photo-1590940485457-413fe8caed47?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTR8fG1vbnN0ZXJhfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60'
  }
]);
</script>

<style >

body {
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
  height: 100%;
  width: 100%;
  margin-bottom: 50px;
  background-color: rgb(244, 201, 186);
}

</style>
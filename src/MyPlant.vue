<template>
   
    <h1>
      {{title}}
    </h1>
    <div class="container">  
     <ul>
      <li v-for="plant in plantes" :key="plant.name">
        <h2>{{ plant.name }}</h2>
        <img :src="plant.image" :alt="plant.name" />

      </li>
    </ul>
  </div>

</template>

<script setup>
// import { ref, reactive } from 'vue';

  defineProps({
    title: {
      type:String,
      required: false,
      default: " 🐠 ",
    },
  });

  const plantes = [
  {
    name: 'Fern',
    image: 'https://images.unsplash.com/photo-1599416024757-71334210456b?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Nnx8ZmVybnxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60'
  },
  {
    name: 'Cactus',
    image: 'https://images.unsplash.com/photo-1554631221-f9603e6808be?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NXx8Y2FjdHVzfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60'
  },
  {
    name: 'Monstera',
    image: 'https://images.unsplash.com/photo-1590940485457-413fe8caed47?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTR8fG1vbnN0ZXJhfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60'
  }
]
  
</script>

<style scoped>
h1 {
  color: rgb(38, 210, 135);
  margin: 100px;
  font-size: 80px;
}
h2{
  color:green;
}
.container {
  display: flex;
  flex-direction: row;
  justify-content: center;
}

ul li {
  display: flex;
  flex-direction: row;
  justify-content: center;
  list-style: none;
  margin-bottom: 100px;
  width:100%;
}
img {
  width: 60%;
  border-radius: 50%;
  border:4px solid greenyellow;
}

</style>
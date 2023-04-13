<template>
  <h1>
    {{ title }}
  </h1>
  <div class="container">
    <div class="box-name">
      <h2 class="plant-name"> {{ props.nameprops.name }}</h2>
    </div>
    <div class="box-img-desc">
      <img :src="props.nameprops.image" :alt="props.nameprops.name" />
      <span class="description">{{ props.nameprops.description }}</span>

    </div>
  </div>
</template>

<script setup>

const props = defineProps({
  title: {
    type: String,
    required: false,
    default: "  🐌 ",
  },
  nameprops: {
    type: Object,
    required: false,
    default: "noname",
  },

});

</script>

<style >
* {
  /* border: 1px solid red; */
}

h1 {
  color: rgb(38, 210, 135);
  margin-bottom: 100px;
  font-size: 80px;
}

h2 {
  color: rgb(183, 63, 99);
  font-size: 32px;
}

.container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  height: 400px;
  width: 80%;
  margin: 0 auto;
}

.box-img-desc {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding:20px;
  height: 390px;
  width:80%;
}

img {
  width: 60%;
  height: 120%;
  border-radius: 50%;
  border: 4px solid greenyellow;
}
.description {
  width: 50%;
  margin-left: 30px;
  color:white;
  font-size: 25px;
}
</style>
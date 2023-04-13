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
    default: " 🐠 ",
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
  margin: 100px;
  font-size: 80px;
}

h2 {
  color: green;
  font-size: 30px;
}

.container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  height: 400px;
  width: 80%;
  margin: 0 auto;
  border: 1px solid rgb(229, 219, 229);

}

.box-name {
  border: 1px solid rgb(255, 225, 0);
}

.box-img-desc {
  border: 1px solid rgb(235, 71, 224);
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding:20px;
  height: 300px;
  width:80%;
}

img {
  width: 60%;
  height: 60%;
  border-radius: 50%;
  border: 4px solid greenyellow;
}
.description {
  width: 50%;
  border: 1px solid rgb(38, 37, 38);
}
</style>
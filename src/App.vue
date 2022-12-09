<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="background">
    <div class="left-content">
      <section class="section-top"></section>
      <section class="section-bottom"></section>

    </div>
    <div class="right-content"></div>
  </div>
</template>

<style scoped>
.left-content {
  width: 70vw;
  height: 100vh;
  background-color: blue;
  flex-direction: column;
}

.left-content .section-top {
  width: 90vw;
  height: 20vh;
  margin-top:20px;
  background-color: yellow;
  flex-direction: row;
}
.left-content .section-bottom {
  width: 90vw;
  height: 75vh;
  margin-top:5vh;
  background-color: pink;
  flex-direction: row;
}

.right-content {
  width: 30vw;
  height: 100vh;
  background-color: red;
}

.background {
  display:flex;
  background-color: rgb(67, 79, 91);
}

.cards {
  background-color: rgb(56, 58, 70);
  border-radius: 10%;
}

.cards .orange-one {
  background-color: rgb(239, 91, 1);
}
.cards .orange-two {
  background-color: rgb(175, 80, 24);
}

.cards .orange-three {
  background-color: rgb(82, 62, 55);
}

</style>

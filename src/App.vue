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
    aaaaaa
    <div class="left-content"></div>
    <div class="right-content"></div>
  </div>
</template>

<style scoped>
.left-content {
  width: 70vw;
  height: 100vh;
  background-color: blue;
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

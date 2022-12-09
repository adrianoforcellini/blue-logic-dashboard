<script setup>
import { GiFarmTractor } from "oh-vue-icons/icons";
components: {
  GiFarmTractor;
}
import Tractor from "vue-material-design-icons/Tractor.vue";
</script>

<template>
  <div class="background">
    <div class="left-content">
      <section class="section-top">
        <div
          class="cards"
          style="width: 5%; display: flex; flex-direction: column;padding:5px"
        >
          <Tractor style="color: white; margin-left: 10%; margin-top:5%" :size="40" />
          <h1 style="margin-left:20%">40</h1>
        </div>
        <div class="cards" style="width: 70%"></div>
        <div class="cards" style="width: 20%"></div>
      </section>
      <section class="section-bottom"></section>
    </div>
    <div class="right-content"></div>
  </div>
</template>

<style scoped>
.left-content {
  width: 70vw;
  height: 100vh;
  flex-direction: column;
}

.left-content .section-top {
  display: flex;
  width: 100%;
  height: 20vh;
  margin-top: 20px;
  flex-direction: row;
}
.left-content .section-bottom {
  width: 100%vw;
  height: 75vh;
  justify-content: space-around;
  margin-top: 5vh;
  flex-direction: row;
}

.right-content {
  width: 30vw;
  height: 100vh;
}

.background {
  display: flex;
  background-color: rgb(67, 79, 91);
  color:white
}

.cards {
  background-color: rgb(56, 58, 70);
  height: 100%;
  border-radius: 25%;
  margin-left: 10px;
  margin-right: 10px;
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

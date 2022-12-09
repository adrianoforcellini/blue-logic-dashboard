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
          class="card"
          style="
            width: 5%;
            display: flex;
            flex-direction: column;
            padding: 5px;
            border-radius: 30px;
          "
        >
          <Tractor
            style="color: white; margin-left: 5%; margin-top: 25%"
            :size="38"
          />
          <h1 style="margin-left: 20%">40</h1>
        </div>
        <div class="card" style="width: 70%; border-radius: 25px"></div>
        <div class="card" style="width: 20%; border-radius: 25px"></div>
      </section>
      <section class="section-bottom">
        <div class="bottom-left">
          <div class="card" style="width: 90%; border-radius: 35px"></div>
        </div>
        <div class="bottom-rigth">
          <div class="top">
            <div class="card" style="width: 50%; border-radius: 50px"></div>
            <div class="card" style="width: 50%; border-radius: 50px"></div>
          </div>
          <div class="bottom">
            <div
              class="card"
              style="border-radius: 50px; margin-top: 15px"
            ></div>
          </div>
        </div>
      </section>
    </div>
    <div class="right-content">
      <div class="card" style="border-radius:30px"></div>
    </div>
  </div>
</template>

<style scoped>

.right-content {
  width: 30vw;
  padding:15px
}

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
  display: flex;
  width: 100%vw;
  height: 75vh;
  justify-content: space-around;
  margin-top: 5vh;
  flex-direction: row;
}

.section-bottom .bottom-left {
  width: 30%;
  height: 90%;
}

.section-bottom .bottom-rigth {
  display: flex;
  flex-direction: column;
  width: 70%;
  height: 100%;
}

.bottom-rigth .top {
  display: flex;
  width: 100%;
  height: 40%;
}

.bottom-rigth .bottom {
  width: 100%;
  height: 40%;
}
.background {
  display: flex;
  background-color: rgb(67, 79, 91);
  color: white;
}

.card {
  display: flex;
  background-color: rgb(56, 58, 70);
  height: 100%;
  margin-left: 10px;
  margin-right: 10px;
}

.card .orange-one {
  background-color: rgb(239, 91, 1);
}
.card .orange-two {
  background-color: rgb(175, 80, 24);
}

.card .orange-three {
  background-color: rgb(82, 62, 55);
}
</style>

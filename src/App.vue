<script setup>
import Tractor from "vue-material-design-icons/Tractor.vue";
import ClockOutline from "vue-material-design-icons/ClockOutline.vue";
import ArrowTopRight from "vue-material-design-icons/ArrowTopRight.vue";
import SpeedometerMedium from "vue-material-design-icons/SpeedometerMedium.vue";
import GasStation from "vue-material-design-icons/GasStation.vue";
import Highcharts from 'highcharts';  

document.addEventListener('DOMContentLoaded', function () {
    Highcharts.chart('container', {
        chart: {
            type: 'bar'
        },
        title: {
            text: 'Fruit Consumption'
        },
        xAxis: {
            categories: ['Apples', 'Bananas', 'Oranges']
        },
        yAxis: {
            title: {
                text: 'Fruit eaten'
            }
        },
        series: [{
            name: 'Jane',
            data: [1, 0, 4]
        }, {
            name: 'John',
            data: [5, 7, 3]
        }],
    });
});
</script>

<template>
  <div class="background">
    <div class="left-content">
      <section class="section-top">
        <div
          class="card"
          style="
            width: 7%;
            display: flex;
            flex-direction: column;
            padding: 5px;
            border-radius: 30px;
            text-align: center;
          "
        >
          <Tractor
            style="color: white; margin-left: 10%; margin-top: 45%"
            :size="46"
          />
          <span style="font-size: 3vw; font-weight: bold">40</span>
        </div>
        <div
          class="card"
          style="width: 70%; border-radius: 25px; flex-direction: column"
        >
          <div
            class="line-one"
            style="
              width: 100%;
              display: flex;
              flex-direction: row;
              margin-top: 10px;
              margin-left: 15px;
              font-weight: bold;
              font-size: 1.1vw;
              text-align: center;
            "
          >
            <ClockOutline :size="46" />
            <div style="width: 15%; margin-left: 70px">
              <span>TEMPO TRABALHANDO</span>
            </div>
            <div style="width: 15%; margin-left: 70px">
              <span>TEMPO OMISSO</span>
            </div>
            <div style="width: 15%; margin-left: 70px">
              <span>TEMPO OSSIOSO</span>
            </div>
          </div>
          <div
            class="line-two orange-three"
            style="
              border-radius: 20px;
              display: flex;
              flex-direction: row;
              margin-top: 10px;
              margin-left: 5px;
              margin-right: 5px;
              padding-left: 15px;
              padding-right: 15px;
              height: 20%;
              font-size: 2vw;
              align-items: center;
            "
          >
            <span>Total</span>
            <div style="width: 15%; margin-left: 65px; text-align: center">
              <span>127 h</span>
            </div>
            <div style="width: 15%; margin-left: 65px; text-align: center">
              <span>15 h</span>
            </div>
            <div style="width: 15%; margin-left: 65px; text-align: center">
              <span>10 h</span>
            </div>
          </div>
          <div
            class="line-three orange-two"
            style="
              border-radius: 20px;
              display: flex;
              flex-direction: row;
              margin-top: 10px;
              margin-left: 5px;
              margin-right: 5px;
              padding-left: 15px;
              padding-right: 15px;
              height: 20%;
              font-size: 1.5vw;
              align-items: center;
            "
          >
            <span>Média</span>
            <div style="width: 15%; margin-left: 65px; text-align: center">
              <span>12,3 h</span>
            </div>
            <div style="width: 15%; margin-left: 65px; text-align: center">
              <span>0,3 h</span>
            </div>
            <div style="width: 15%; margin-left: 65px; text-align: center">
              <span>0,2 h</span>
            </div>
          </div>
        </div>
        <div
          class="card"
          style="
            width: 20%;
            border-radius: 25px;
            display: flex;
            flex-direction: column;
            align-itens: center;
            text-align: center;
            font-weight: bold;
          "
        >
          <div style="font-size: 1.3vw; margin-top: 10%">
            EFICIÊNCIA OPERACIONAL
          </div>
          <div style="font-size: 3vw">82%</div>
          <div><ArrowTopRight :size="46" /></div>
        </div>
      </section>
      <section class="section-bottom">
        <div class="bottom-left">
          <div
            class="card"
            style="
              width: 90%;
              border-radius: 35px;
              display: flex;
              flex-direction: column;
              font-weight: bold;
              text-align: center;
            "
          >
            <span style="font-size: 1.3vw; margin-top: 10px">COMBUSTÍVEL</span>
            <div style="display: flex; flex-direction: row; margin-top: 10px">
              <div
                style="
                  width: 50%;
                  height: 15vh;
                  border-right: 1px solid white;
                  display: flex;
                  flex-direction: column;
                "
              >
                <span style="font-size: 2vw;margin-top:5px">1000</span>
                <span style="font-size: 2vw;margin-top:5px">L</span>
                <span style="font-size: 1.3vw;margin-top:5px">Total</span>
              </div>
              <div
                style="
                  width: 50%;
                  height: 10vh;
                  display: flex;
                  flex-direction: column;
                "
              >
                <span style="font-size: 2vw;margin-top:5px">16,3</span>
                <span style="font-size: 2vw;margin-top:5px">L/h</span>
                <span style="font-size: 1.3vw;margin-top:5px">Média</span>
              </div>
            </div>
            <div id="container" style="height: 300px"></div>
          </div>
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
      <div class="card" style="border-radius: 30px"></div>
    </div>
  </div>
</template>

<style scoped>
.right-content {
  width: 30vw;
  padding: 15px;
}

.left-content {
  width: 70vw;
  height: 100vh;
  flex-direction: column;
}

.left-content .section-top {
  display: flex;
  width: 100%;
  height: 25vh;
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

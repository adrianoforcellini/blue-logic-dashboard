<script setup>
import Tractor from "vue-material-design-icons/Tractor.vue";
import ClockOutline from "vue-material-design-icons/ClockOutline.vue";
import ArrowTopRight from "vue-material-design-icons/ArrowTopRight.vue";
import SpeedometerMedium from "vue-material-design-icons/SpeedometerMedium.vue";
import GasStation from "vue-material-design-icons/GasStation.vue";
import Highcharts from "highcharts";

document.addEventListener("DOMContentLoaded", function () {
  Highcharts.chart("container", {
    chart: {
      type: "bar",
      backgroundColor: "none",
    },
    colors: ["#ef5b01"],
    title: {
      text: "L/t",
    },
    xAxis: {
      categories: ["F1", "F2", "F3"],
    },

    series: [
      {
        data: [63, 65, 80],
      },
    ],
  });

  Highcharts.chart("line-container", {
    chart: {
      backgroundColor: "none",
      style: { color: "white", fill: "white" },
    },
    title: {
      text: "Gráfico de Eficiência",
    },
    colors: ["white", "#008036"],

    subtitle: {
      align: "left",
    },
    legend: false,

    yAxis: {
      title: {},
      type: "linear",
      categories: ["0", "50", "100", "150", "200"],
    },

    xAxis: {
      type: "datetime",
      categories: [
        "06:00",
        "07:00",
        "08:00",
        "09:00",
        "10:00",
        "11:00",
        "12:00",
        "13:00",
        "14:00",
        "15:00",
        "16:00",
      ],
    },

    legend: {
      layout: "vertical",
      align: "right",
      verticalAlign: "middle",
    },

    // plotOptions: {
    //     series: {
    //         label: {
    //             connectorAllowed: false
    //         },
    //     }
    // },

    series: [
      {
        name: "TCH",
        data: [110, 149, 153, 154, 100, 148],
        showInLegend: false,
      },
      {
        name: "Eficiência Operacional",
        data: [80, 83, 98, 99, 82, 84],
        showInLegend: false,
      },
    ],

    responsive: {
      rules: [
        {
          condition: {
            maxWidth: 500,
          },
          chartOptions: {
            legend: {
              layout: "horizontal",
              align: "center",
              verticalAlign: "bottom",
            },
          },
        },
      ],
    },
  });
  const texts = document.getElementsByTagName("text");
  for (let text of texts) {
    text.setAttribute("style", "color:white");
    text.setAttribute("style", "fill:white");
  }

  let spams = Array.from(texts).filter(span => span.innerHTML === 'Highcharts.com')
  for ( let spam  of spams) {
    spam.innerHTML=""
  }

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
                <span style="font-size: 2vw; margin-top: 5px">1000</span>
                <span style="font-size: 2vw; margin-top: 5px">L</span>
                <span style="font-size: 1.3vw; margin-top: 5px">Total</span>
              </div>
              <div
                style="
                  width: 50%;
                  height: 10vh;
                  display: flex;
                  flex-direction: column;
                "
              >
                <span style="font-size: 2vw; margin-top: 5px">16,3</span>
                <span style="font-size: 2vw; margin-top: 5px">L/h</span>
                <span style="font-size: 1.3vw; margin-top: 5px">Média</span>
              </div>
            </div>
            <div
              id="container"
              style="height: 40vh; background-color: none"
              onmouseover="transformTheColorsOfTheGraph"
            ></div>
            <div
              class="orange-two"
              style="
                position: absolute;
                bottom: 1vh;
                width: 16.5vw;
                border-radius: 20px;
                height: 10vh;
                margin-left: 1vw;
                display: flex;
                padding-top: 1vh;
              "
            >
              <div
                style="
                  display: flex;
                  flex-direction: column;
                  width: 30%;
                  text-align: center;
                  font-size: 1.7vw;
                  margin-left: 2vw;
                "
              >
                <span>0,89</span>
                <span>L/t</span>
              </div>
              <GasStation :size="48" style="margin-left: 2vw" />
            </div>
          </div>
        </div>
        <div class="bottom-rigth">
          <div class="top">
            <div
              class="card"
              style="
                width: 50%;
                border-radius: 50px;
                display: flex;
                flex-direction: column;
                text-align: center;
                alignt-itens: center;
                font-size: 1.5vw;
                font-weight: bold;
              "
            >
              <span style="margin-top: 3vh"> RPM </span>
              <div
                class="orange-two"
                style="
                  margin-top: 3vh;
                  border-radius: 15px;
                  width: 90%;
                  align-self: center;
                  padding: 2%;
                "
              >
                <span>MOTOR </span>
                <span> 1452</span>
              </div>
              <div
                class="orange-two"
                style="
                  padding: 2%;
                  margin-top: 3vh;
                  border-radius: 15px;
                  width: 90%;
                  align-self: center;
                "
              >
                <span>EXTRATOR </span>
                <span> 850</span>
              </div>
            </div>
            <div
              class="card"
              style="
                width: 50%;
                border-radius: 50px;
                display: flex;
                flex-direction: column;
                text-align: center;
                alignt-itens: center;
                font-size: 1.5vw;
                font-weight: bold;
              "
            >
              <span style="margin-top: 3vh"> VELOCIDADE </span>
              <div
                class="orange-two"
                style="
                  margin-top: 3vh;
                  border-radius: 35px;
                  width: 80%;
                  align-self: center;
                  padding: 2%;
                "
              >
                <div
                  style="
                    display: flex;
                    flex-direction: row;
                    justify-content: space-around;
                    align-itens: center;
                    font-size: 2vw;
                  "
                >
                  <div style="display: flex; flex-direction: column">
                    <span>5,3 </span>
                    <span> Km/h</span>
                  </div>
                  <SpeedometerMedium :size="56" />
                </div>
              </div>
            </div>
          </div>
          <div class="bottom">
            <div
              class="card"
              style="
                border-radius: 50px;
                margin-top: 15px;
                display: flex;
                flex-direction: column;
              "
            >
              <div
                style="
                  position: absolute;
                  background-color: rgb(56, 58, 70);
                  height: 5%;
                  width: 35vw;
                  z-index: 10000;
                  margin-left: 5%;
                "
              >
                <div style="display: flex; margin-top: 1vw">
                  <div
                    style="
                      background-color: #008036;
                      width: 1.3vw;
                      height: 1.3vw;
                      margin-left: 10%;
                    "
                  />
                  <span style="margin-left:3%">EFICIÊNCIA OPERACIONAL</span>
                  <div
                    style="
                      background-color: white;
                      width: 1.3vw;
                      height: 1.3vw;
                      margin-left: 10%;
                    "
                  />
                  <span style="margin-left:3%">THC</span>

                </div>
              </div>
              <div id="line-container" style="width: 100%; height: 90%"></div>
            </div>
          </div>
        </div>
      </section>
    </div>
    <div class="right-content">
      <div
        class="card"
        style="
          border-radius: 30px;
          display: flex;
          flex-direction: column;
          font-size: 1.5vw;
          font-weight: bold;
        "
      >
        <div
          style="border-bottom: 1px solid white; display: flex; margin-top: 3%"
        >
          <div
            style="
              background-color: #008036;
              width: 1vw;
              height: 100%;
              margin-left: 10%;
            "
          />
          <span style="margin-left: 5%">ÁREA TRABALHADA</span>
        </div>
        <img src="./assets/map.png" style="margin: 3%; margin-top: 10%" />
        <div style="width: 100%; margin-left: 7vw">
          <span style="margin-left: 1vw">TOTAL:</span>
          <span style="color: #008036">1250 ha</span>
        </div>
      </div>
    </div>
  </div>
</template>
methods: { },

<style scoped>
text {
  color: white;
}
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
  font-family: "Verdana, Arial";
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

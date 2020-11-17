<template>
  <div class="">
    <!-- <div class="chart-panel mt-8 mr-auto ml-auto">
      <LineChart :chartdata="dataCollection" :options="chartOptions" />
    </div> -->
    <div class="card-panel">
      <StatisticsCard :figure="200" text="Total clicks" />
      <StatisticsCard :figure="30" text="Total links" />
      <StatisticsCard :figure="60" text="Top referrer" />
      <StatisticsCard :figure="10" text="Top link" />
    </div>

    <div class="flex flex-wrap mt-6 bg-black">
      <div class="w-full lg:w-1/2 pr-0 lg:pr-2">
        <p class="text-xl pb-3 flex items-center">
          <i class="fas fa-plus mr-3"></i> Monthly Reports
        </p>
        <div class="p-6 bg-black">
          <LineChart :chartdata="dataCollection" :options="chartOptions" />
        </div>
      </div>
      <div class="w-full lg:w-1/2 pl-0 lg:pl-2 mt-12 lg:mt-0">
        <p class="text-xl pb-3 flex items-center">
          <i class="fas fa-check mr-3"></i> Resolved Reports
        </p>
        <div class="p-6 black">
          <LineChart :chartdata="dataCollection" :options="chartOptions" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import LineChart from "./chart/line.js";
import StatisticsCard from "./statistics-card.vue";
export default {
  name: "Overview",
  components: {StatisticsCard, LineChart },
  data() {
    return {
      chartOptions: {
        legend: false,
        responsive: true,
        maintainAspectRatio: false,
        scales: {
          xAxes: [
            {
              gridLines: { display: false },
            },
          ],
          yAxes: [
            {
              gridLines: { display: true },
            },
          ],
        },
      },
      dataCollection: {
        labels: ["One", "Two", "Three"],
        datasets: [
          {
            label: "Data One",
            borderColor: "#087979",
            backgroundColor: "#fff0",
            pointRadius: 5,
            data: [10, 40, 0],
          },
          {
            label: "Data One",
            borderColor: "#f84f79",
            backgroundColor: "#fff0",
            pointRadius: 5,
            data: [30, 20, 40],
          },
          {
            label: "Data One",
            borderColor: "#f879ca",
            backgroundColor: "#fff0",
            pointRadius: 5,
            data: [34, 2, 23],
          },
        ],
      },
    };
  },
};
</script>

<style scoped>
/* .card-panel {
  padding: 3px 13px;
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
}

.chart-panel {
  width: 90%;
}

@media (max-width: 650px) {
  .card-panel {
    flex-wrap: wrap;
    
  }
} */
</style>

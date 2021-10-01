<template>
  <div class="container">
    <h1 class="title" v-if="loaded">Coffee (Robustas) Average NY and Le Havre/Marseilles Market Price</h1>
    <div class="Chart_title" v-if="loaded">
      US Dollar per Kilogram ($ / kg)
    </div>
    <div class="error-message" v-if="showError">
      {{ errorMessage }}
    </div>
    <line-chart
      v-if="loaded"
      :chartData="prices"
      :chart-labels="labels"
      :options="options"/>
  </div>
</template>

<script>
import LineChart from './CommodityChart.vue'

export default {
  name: 'LineChartContainer',
  components: {LineChart},
  data: () => ({
    loaded: false,
    prices: [],
    labels: [],
    showError: false,
    errorMessage: 'Error building graph',
    options: {
      scales: {
        yAxes: [{
          ticks: {
            beginAtZero: true
          },
          gridLines: {
            display: true
          }
        }],
        xAxes: [{
          gridLines: {
            display: false
          }
        }],
        legend: {
          display: false
        },
        responsive: true,
        maintainAspectRatio: false,
      },
    }
  }),
  async mounted() {
    this.loaded = false
    try {
      const pricesList = await fetch('https://alphavantageworker.jacob1725.workers.dev', {
        method: 'GET',
        headers: {
          'Content-Type': 'application/json',
          'Key': "Coffee"
        },
        mode: 'cors'
      }).catch((err) => {
        this.showError = true
        console.error(err)
      })
      const priceListData = await pricesList.json()
      for (let i = 0; i < priceListData.length; i++) {
        this.prices.push(priceListData[i].price)
      }
      for (let i = 0; i < priceListData.length; i++) {
        this.labels.push(priceListData[i].date)
      }
      this.loaded = true
    } catch (e) {
      console.error(e)
    }
  }
}
</script>

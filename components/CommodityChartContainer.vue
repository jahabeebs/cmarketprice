<template>
  <div class="container">
    <div class="title text-center md:text-2xl sm:text-xs" v-if="loaded">Robustas Average NY and Le Havre/Marseilles
      Market Price
    </div>
    <div class="Chart_title text-center md:text-2xl sm:text-xs" v-if="loaded">
      US Dollar per Kilogram
    </div>
    <div class="md:text-lg text-center" v-if="loaded">
      Most recent price: <span class="font-bold">${{ this.prices[this.prices.length - 1] }}/kg</span> on <span
        class="font-bold">{{ this.labels[this.labels.length - 1] }}</span>
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

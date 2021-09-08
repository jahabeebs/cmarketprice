<template>
  <div class="container">
    <line-chart
      v-if="loaded"
      :chartData="chartData"
      :options="options"/>
  </div>
</template>

<script>
import LineChart from './CommodityChart.vue'

export default {
  name: 'LineChartContainer',
  components: { LineChart },
  data: () => ({
    loaded: false,
    chartData: null
  }),
  async mounted () {
    this.loaded = false
    try {
      const { userList } = await fetch('https://alphavantageworker.jacob1725.workers.dev', {
        method: 'GET',
        headers: {
          'Content-Type': 'application/json',
          'Key': 'Coffee'
        },
        mode: 'cors'
      });
      this.chartData = userList
      this.loaded = true
    } catch (e) {
      console.error(e)
    }
  }
}
</script>
